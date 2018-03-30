<head>
	<style>
		html, body {
			font-family: Helvetica, Verdana;
		}


		h1 {
			margin: 0;
		}

		h2 {
			margin-top: 80px;
		}

		h3 {
			margin-top: 0;
		}

		.obs {
			color: #f33;
			font-style: italic;
		}

		.task {
			margin: 20px 0;
			padding: 10px;
			border: 1px dotted #ccc;
			border-radius: 5px;
			background-color: #fafafa;
		}
	</style>
</head>

Moduler / micro services i MakerAdmin v0.1
==========================================

<div id="content">
	<p class="obs">OBS: Denna lista är inte uppdaterad på väldigt länge och stämmer inte överens med verkligheten.</p>

	<div class="task">
		<h3>Frontend</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Frontend">https://github.com/MakersOfSweden/MakerAdmin-Frontend</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p>Javascript frontend baserat på följande tekniker:</p>
		<ul>
			<li>Webpack</li>
			<li>React</li>
			<li>Backbone</li>
		</ul>
	</div>

	<div class="task">
		<h3>API gateway</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-ApiGateway">https://github.com/MakersOfSweden/MakerAdmin-ApiGateway</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Agerar den centrala punkten för API-anrop</li>
			<li>Vidarebefodrar API-anropet till rätt micro service</li>
			<li>Sköter autentisering och lägger på headers som att indikerar behörighetsnivå på alla API-anrop</li>
			<li>Registrerar när tjänster startar och stoppar och för en lista över dessa</li>
			<li>Loggar inkommande och utgående datatrafik</li>
			<li>Skickar felmeddelanden till klient om en micro service är nere när ett API-anrop görs</li>
			<li>Konverterar API-responses till angivet format (JSON, XML, *.csv, etc)</li>
			<li>"Facades" - möjlighet att skapa en virtuell API endpoint som aggregerar data från flera micro services till ett svar</li>
		</ul>
		<p class="wantlist">Önskvärda funktioner för framtiden:</p>
		<ul>
			<li>Second factor via YubiKey</li>
			<li>Lastbalanserar</li>
			<li>Skickar larm till en administratör om en micro service går ner</li>
			<li>Övervakar att tjänsterna är igång och fungerar</li>
			<li>Om en microservice är otillgänglig går det i vissa fall att köra fallback på en äldre version</li>
			<li>Köar API-anrop under korta stunder medans tjänster startar (Hanterar hotswap)</li>
		</ul>
	</div>

	<div class="task">
		<h3>Medlemsregister + grupper</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Membership">https://github.com/MakersOfSweden/MakerAdmin-Membership</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Körs på nationell nivå - alla medlemmar ligger i ett nationellt register</li>
			<li>En medlem kan vara medlem i flera olika föreningar</li>
			<li>Varje förening får en grupp där medlemmen läggs till</li>
			<li>Varje förening får möjlighet att lägga till egna subgrupper för att ytterligare kategorisera användare</li>
			<li>Medlemmar kan ha behörighet att komma åt medlemmar i dessa subgrupper för att till exempel en arbetsgrupp/intressegrupp skall kunna göra ett mailutskick</li>
		</ul>
	</div>

	<div class="task">
		<h3>Ekonomi</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Economy">https://github.com/MakersOfSweden/MakerAdmin-Economy</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Hanterar alla monetära transaktioner</li>
			<li>Har en struktur som är uppbyggd som ett bokföringssystem enligt svensk standard</li>
			<li>Går att föra enklare bokföring i (Konton, verifikationer, transaktioner, huvudbok, enklare rapporter)</li>
			<li>Stödjer SIE export/import</li>
		</ul>
	</div>

	<div class="task">
		<h3>Fakturering</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Invoice">https://github.com/MakersOfSweden/MakerAdmin-Invoice</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Gör det möjligt att skapa fakturor och exportera dessa i lämpligt format (HTML, PDF, JSON, Text)</li>
			<li>Utmärkt komplement till ekonomi-modulen, men går även att köra självständigt</li>
			<li>Genererar och lagrar OCR-nummer, fakturanummer och liknande</li>
		</ul>
	</div>

	<div class="task">
		<h3>RFID</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-RFID">https://github.com/MakersOfSweden/MakerAdmin-RFID</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>En databas över samtliga nycklar som är utlämnade</li>
			<li>En nyckel har en koppling till medlem</li>
			<li>En medlem kan ha flera nycklar</li>
			<li>För ett register över RFID-taggar och dess giltighetstider</li>
			<li>Behörighetsnivåer sker via modulen "Medlemsregister + grupper"</li>
			<li>Visa lista på alla nycklar (Filtrering: Samtliga, endast aktiva, endast passerat slutdatum, endast sådana som aldrig har aktiverats)</li>
			<li>Giltighetstider beräknas fram från monetära transaktioner.</li>
			<li>Man ska kunna göra undantag och aktivera nycklar utan monetär transaktion. Dessa ska synas i en separat lista och ha en kommentar om varför de är aktiva utan betalning (Till exempel styrelse, städare, hantverkare eller andra med förtroendeuppdrag)</li>
		</ul>
	</div>

	<div class="task">
		<h3>Försäljning</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Sales">https://github.com/MakersOfSweden/MakerAdmin-Sales</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Möjlighet att skapa produkter</li>
			<li>Försäljning av produkter</li>
			<li>Prenumerationer</li>
			<li>Koppling till betalsystem</li>
			<li>Lagersaldo</li>
		</ul>
	</div>

	<div class="task">
		<h3>Utskick / sändkö</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-SendQueue">https://github.com/MakersOfSweden/MakerAdmin-SendQueue</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Möjlighet att göra ett "utskick" till en medlem, grupp, E-postadress, telefonnummer, etc</li>
			<li>Lagrar utskicket i en databas och flaggar det som köat</li>
			<li>En annan micro service går igenom denna databas och gör själva utskicket på lämpligt vis</li>
		</ul>
	</div>

	<div class="task">
		<h3>SMS sender</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-SMSSender">https://github.com/MakersOfSweden/MakerAdmin-SMSSender</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Läser igenom sänd-kön och skickar iväg själva SMS:et genom <a href="https://www.46elks.com/">https://www.46elks.com/</a></li>
			<li>Låter meddelandet ligga kvar i databasen, men flaggar det som skickat</li>
		</ul>
	</div>

	<div class="task">
		<h3>Mail sender</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-MailSender">https://github.com/MakersOfSweden/MakerAdmin-MailSender</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Läser igenom sänd-kön och skickar iväg själva E-postmeddelandet genom <a href="https://www.mailgun.com/">https://www.mailgun.com/</a></li>
			<li>Låter meddelandet ligga kvar i databasen, men flaggar det som skickat</li>
		</ul>
	</div>

	<div class="task">
		<h3>Statistik</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Statistics">https://github.com/MakersOfSweden/MakerAdmin-Statistics</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Aggregerar data från de olika modulerna och kombinerar denna på ett sätt som gör att man kan rita diagram och presentera statistik</li>
		</ul>
	</div>

	<div class="task">
		<h3>Passersystem</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Keycard">https://github.com/MakersOfSweden/MakerAdmin-Keycard</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Hämtar data från de olika modulerna ("RFID", "Medlemsregister + grupper" och "Ekonomi") för att sedan beräkna fram aktuellt status på en nyckel och sedan generera data för att importera i ett externt passersystem.</li>
		</ul>
	</div>

	<div class="task">
		<h3>CRM</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-CRM">https://github.com/MakersOfSweden/MakerAdmin-CRM</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Möjlighet att skapa generisk data</li>
			<li>Möjlighet att koppla denna data till en annan entitet i systemet</li>
			<li>Kategorisering / tags eller på något annat vis strukturera data</li>
			<li>Todo-listor med tasks kopplade till medlem</li>
		</ul>
	</div>

	<div class="task">
		<h3>Testdata</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Testdata">https://github.com/MakersOfSweden/MakerAdmin-Testdata</a></dd>
			<dt>Status</dt>
			<dd>Utvecklingsarbete pågår</dd>
		</dl>
		<p>För att kunna jobba vettigt i en utvecklingsmiljö krävs testdata. Det är även bra med ordentligt data när man skall visa upp systemet för någon som är intresserad av att köra det. För detta behöver vi kunna generera testdata i lagom mängd.</p>
	</div>

	<div class="task">
		<h3>Dokumenthantering</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-DocumentManagement">https://github.com/MakersOfSweden/MakerAdmin-DocumentManagement</a></dd>
			<dt>Status</dt>
			<dd>Planerad modul för framtiden</dd>
		</dl>
		<p>Ett superenkelt dokumentarkiv som fungerar som så att man laddar upp filer och sorterar in manuellt via FTP. Ett PHP-script läser denna katalogstruktur och skapar en sida där man kan klicka runt. Självklart med automatiskt generering av thumbnails från bilder och pdf. På sikt uppladdning via webgränssnitt.</p>
	</div>

	<div class="task">
		<h3>Tictail import</h3>
		<ul>
			<li>Laddar hem ordrar från Tictail's API och sprar dessa som *.json i en lokal mapp</li>
			<li>Går igenom dessa *.json och genererar verifikationer att skicka in i ekonomi-modulen</li>
			<li>Klassificering för att bokföra saker på rätt konto</li>
			<li>Försöker matcha E-post eller telefonnummer mot befintlig medlem</li>
		</ul>
	</div>

	<div class="task">
		<h3>Kioskinterface</h3>
		<dl>
			<dt>GitHub</dt>
			<dd>N/A</dd>
			<dt>Status</dt>
			<dd>Planerad modul för framtiden</dd>
		</dl>
		<p>Vi bygger ett gränssnitt som är lämpligt för att någon förtroendevald ska få åtkomst endast till de funktioner och data som krävs för att lämna ut en nyckel till en medlem.</p>
	</div>

	<div class="task">
		<h3>Integration: Stripe</h3>
		<p></p>
	</div>

	<div class="task">
		<h3>Integration: PayPal</h3>
		<p></p>
	</div>




	<h2>Moduler planerade för framtiden</h2>

	<div class="task">
		<h3>Integration: BitPay</h3>
		<p>Önskvärd funktion i framtiden, men inget planerat inom kort.</p>
	</div>

	<div class="task">
		<h3>Integration: Autogiro</h3>
		<p>Önskvärd funktion i framtiden, men inget planerat inom kort.</p>
	</div>

	<div class="task">
		<h3>SEB / Bankgiro-import</h3>
		<p>På kort sikt klurar vi ut hur man parse:ar ut Bankgiro-data från SEB's internetbank. Det verkar inte finnas någon exportfunktion för detta, så vi får nog köra lite regular expressions mot en *.html-fil.</p>
		<p>På lång sikt kör vi med SEB's "riktiga" API</p>
		<ul>
			<li>Laddar hem och parse:ar *.html från SEB</li>
			<li>En kontroll görs mot databasen för att se vilken data som är ny (matchat mot datum + transaktions-ID från banken).</li>
			<li>De rader som är nya petas in in en JSON-array som skickas till frontend</li>
			<li>Användaren får godkänna att dessa rader stoppas in i databasen</li>
			<li>När användaren godkänner skickas en JSON-array tillbaka, allting i denna array läggs in i databasen</li>
		</ul>
	</div>

	<div class="task">
		<h3>Kalendarium</h3>
		<dl>
			<dt>GitHub</dt>
			<dd><a target="_blank" href="https://github.com/MakersOfSweden/MakerAdmin-Calendar">https://github.com/MakersOfSweden/MakerAdmin-Calendar</a></dd>
			<dt>Status</dt>
			<dd>Planerad modul för framtiden</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Möjlighet att skapa flera olika kalendrar</li>
			<li>Olika behörighetsnivåer på kalendrarna</li>
			<li>Skapa event i en kalender</li>
			<li>Exportera kalendrar/event i lämpligt format (JSON, *.ics)</li>
		</ul>
	</div>

	<div class="task">
		<h3>Villkårade priser</h3>
		<dl>
			<dt>GitHub</dt>
			<dd>N/A</dd>
			<dt>Status</dt>
			<dd>Planerad modul för framtiden</dd>
		</dl>
		<p class="features">Grundläggande funktioner:</p>
		<ul>
			<li>Mängdrabatt</li>
			<li>Datumstyrda priser</li>
			<li>Intervallstyrda priser</li>
			<li>Kombinationsrabatt</li>
			<li>Övriga externa krav (arbetslös, student, etc)</li>
			<li>Pris baserat på grupptillhörighet</li>
		</ul>
	</div>
</div>

<!--
Config
	Bygg ett gränssnitt som gör det möjligt att redigera config-tabellen direkt från webben

Interna webbsidor: Föreningsinformation, wiki, forum 

EconomyParser
	The EconomyParser interface defines an interface used for importing and converting data from an external system.

	To add a payment system you should do the following:
	* Create a class that implements the EconomyImporter interface
	* Create glue-logic used to read the data, like parsing a *.csv file or connecting to your payment providers API and export data.
	* Go through the data and convert it into a format that could be handled by the system
	* Specify on what account, in the "BAS kontoplan", this transaction should be added to.

EconomyImporter
	This class is used to cross check what is already in the database and what should be imported. All information is kept, but a flag is added to indicate whetever the transaction should be imported into the database or not.

EconomyClassification
	This is a interface used to classificate an economy transaction. When a transaction is imported into the system an accounting instruction (Swe: Verifikation) is automatically created. This accounting instruction need to have at least two rows that defines credit and debit on two different accounts. For example the credit could be on the "1930 Bank account. That information should already have been added by the EconomyImporter class. The debit could be on the "xxxx Membership fee". That should be added by this class. The sum of the transaction should be zero.

	All transaction that cannot be classified is automatically added to the "2999 OBS" account. This account is specified in the "BAS kontoplan" to be used for unclassified or temporary transaction. Everything on this account should be moved in the near future and the balance should be zero.
-->