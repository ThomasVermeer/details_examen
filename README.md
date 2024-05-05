Conventies = afspraken van het schrijven van code.
Werkafspraken = afspraken binnen het team.
DoD = Userstories wanneer ze voldaan/done zijn en gereviewd kan worden door iemand anders. opgeleverde code voldoet aan de convensties.
Alles moet voldoen aan de acceptatiecriteria.
Userstory = Als wil, zodat. Iets van een scructuur erbij.(product backlog in sprint backlog). Uitleggen waarom deze userstory gekoze is.
Acceptatiecriteria wanneer een userstory af is. minimaal 4 per 5.
Planning = (Product backlog, Sprint, backlog, To do, In progress, Ready review, In review, Done). Plan bord actief bijhouden.
Wireframes = Paar userstories natekenen. Flow van een userstory. Homepage, loginpage, dashboard (userstories).
Activiteitendiagram = Activiteit van een specefieke functienaliteit die complexer is. Activiteitendiagram verdeeld in rollen. Start, eind, activiteit en beslissing.
ERD = PK naar FK relatie lijn.
Sitemap = weergave van navigatie.
Code = code moet overal hetzelfde (consident zijn). Comments gebruiken bij complexe. Variabele moet betekenis (duidelijk zijn).
Git = Commit moet duidelijk zijn. Branches werken. 
Daily standups = Vertellen wat je gisteren hebt gedaan, vandaag gaat doen en eventuele problemen. Max 10 a 15 minuten. Ook meereageren en niet alleen luisteren.
Tests = Alle acceptatiecriteria moet terug komen. Technishe tests van edges. Uit de tests opmerkingen en rapportage.
Retro = Bespreken wat goed en slecht ging en hoe kan het beter. Je moet meer de diepte in.
Presentatie/oplevering = Niet te veel bezig zijn met je laptop maar echt aan de persoon. Niet te veel op de foutmelding gaan. Presenteer het opgeleverde werk.
Je moet later ook code vertellen ook van andere. Ook vertellen stel als je meer tijd had.





om rollen aan te maken

Schema::create('users', function (Blueprint $table) {
            $table->id();
            $table->string('name');
            $table->string('email')->unique();
            $table->timestamp('email_verified_at')->nullable();
            $table->string('password')->nullable();
            $table->enum('role', ['Admin', 'User', 'Finance', 'Sales', 'Maintenance', 'Inventory', 'Customer', 'Headmaintenance'])->default('User');
            $table->integer('company_id')->references('id')->on('companies')->nullable();
            $table->rememberToken();
            $table->timestamps();
        });


in de authentication controller
