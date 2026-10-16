<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<title>Gustavs CV</title>

		<!-- Monocraft används om fontfilen finns lokalt på datorn. -->
		<style>
@font-face {
	font-family: "Monocraft";
	src: local("Monocraft"), local("Monocraft Nerd Font");
	font-style: normal;
	font-weight: 100 900;
	font-display: swap;
}

		:root {
			color-scheme: light;
			--bg: #fbf1c7;
			--panel: #f2e5bc;
			--fg: #3c3836;
			--muted: #7c6f64;
			--border: #d5c4a1;
			--accent: #b57614;
		}

* { box-sizing: border-box; }

body {
	margin: 0;
	padding: 32px 20px 56px;
	color: var(--fg);
	font-family: "Monocraft", "DejaVu Sans Mono", monospace;
	font-size: 14px;
	line-height: 1.7;
}

		header, main {
			width: min(100%, 1200px);
			margin-inline: auto;
		}

		.cv-layout {
			display: grid;
			grid-template-columns: 1.3fr 1fr;
			align-items: start;
		}

		.cv-column {
			min-width: 0;
			padding: 24px;
			background: #fbf1c7;
			font-size: 14px;
			line-height: 1.35;
		}

		header { margin-bottom: 20px; }

		h1 {
			margin: 0 0 6px;
			font-size: 1.35rem;
			font-weight: 700;
		}

		.hint {
			margin: 0;
			color: var(--muted);
			font-size: .85rem;
		}

		.toolbar {
			display: flex;
			flex-wrap: wrap;
			align-items: center;
			gap: 10px;
			margin: 18px 0 10px;
		}

		button {
			border: 1px solid var(--border);
			border-radius: 6px;
			padding: 8px 12px;
			background: var(--panel);
			color: var(--fg);
			font: inherit;
			cursor: pointer;
		}

		button:hover { border-color: var(--accent); }

		.editor-shell {
			overflow: auto;
			border: 1px solid var(--border);
			border-radius: 8px;
			background: #fbf1c7;
			box-shadow: 0 4px 18px rgb(60 56 54 / 8%);
		}

		/* Gruvbox Light-inspirerad editor-yta */
		.cv-column a.md-link {
			color: #076678;
			text-decoration: underline;
			text-underline-offset: 2px;
			cursor: pointer;
		}

		.cv-column a.md-link:hover {
			color: #af3a03;
		}

		.cv-column a.md-link:focus-visible {
			outline: 2px solid var(--accent);
			outline-offset: 2px;
		}

		#cv {
			min-height: 65vh;
			margin: 0;
			padding: 24px 28px;
			outline: none;
			white-space: pre-wrap;
			overflow-wrap: anywhere;
			word-break: normal;
			tab-size: 2;
			font-family: "Monocraft", "DejaVu Sans Mono", monospace;
			font-size: 13px;
			line-height: 1.75;
			color: #3c3836;
			caret-color: #af3a03;
		}

		#cv:focus { box-shadow: inset 0 0 0 1px #d5c4a1; }

		/* Highlight.js Gruvbox Light, med färger anpassade för Markdown */
		.hljs { color: #3c3836; background: #fbf1c7; }
		.hljs-section, .hljs-title, .hljs-name { color: #b57614; font-weight: 700; }
		.hljs-strong { color: #af3a03; font-weight: 700; }
		.hljs-emphasis { color: #427b58; font-style: italic; }
		.hljs-bullet, .hljs-symbol, .hljs-link { color: #076678; }
		.hljs-quote { color: #79740e; font-style: italic; }
		.hljs-code, .hljs-keyword, .hljs-selector-tag { color: #8f3f71; }
		.hljs-string, .hljs-attr { color: #79740e; }
		.hljs-meta, .hljs-comment { color: #928374; }
		.hljs-🏷️ { color: #b57614; }
		.hljs-addition { color: #427b58; }
		.hljs-deletion { color: #9d0006; }

		@media (max-width: 600px) {
			body { padding: 20px 12px 36px; }
			#cv { padding: 16px; font-size: 12px; }
		}
		</style>
		<link rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/@highlightjs/cdn-assets@11.10.0/styles/gruvbox-light.min.css">
	</head>
	<body>

		<main>
			<div class="editor-shell">
				<!--
					Klistra in Markdown här. Behåll id="cv".
					Eftersom detta är en HTML-tagg behöver bokstavliga < och > skrivas
					som &lt; och &gt; i den ursprungliga HTML-källan.
				-->
				<div id="cv" class="language-markdown cv-layout" 
										 aria-label="Markdown-källa" aria-multiline="true"
																								 spellcheck="false">
					<div id="cv-left" class="cv-column language-markdown">
# Gustav Johansson - Curriculum vitae
Snäll och kreativ civilingenjör som söker nya utmaningar!

## Avklarade utbildningar
Nedan följer ett urval av utbildnignar och kurser jag genomfört med godkänd examen / certifikat.

### Civilingenjör i Interaktion och Design : 300hp
Umeå Universitet
Augusti 2021 - Juni 2026
[Examensbevis](https://drive.google.com/file/d/1UN3CTVk45YqOhxHUOXJWm2tPWr9Z9bQG/view?usp=sharing)
[Betyg](https://drive.google.com/file/d/19FdlFK9ajPzYNpE5tkYidF1lXsbUsk_Q/view?usp=sharing)
Examensarbete utfärdat i samarbete med Toontrack AB, VT 2026
Detta program är väldigt välanpassat för mig då jag både har ett stort intresse för datavetenskap samt är en väldigt kreativ själ. Under de 5 åren specialiserade jag mig på att möta användarnas behov med ett öppet öra och stor nyfikenhet. Jag valde ett mer programmerings- och datavetenskapligt fokus under andra halvan där jag bland annat läste kurser i datorgrafik, datorsäkerhet, datasekretess, IoT, programvaruteknik, avancerade databassystem och systemnära programmering.

### Militär grundutbildning : 11 månader
Ledningsregementet, Enköping
Augusti 2019 - Juni 2020 
Ledning/Sambandssoldat i Trosspluton

### Estetiska programmet : Musik
Midgårdsskolan, Umeå
Augusti 2016 - Juni 2019

### Ledarutbildning : Svenska kyrkan
Sävar-Holmöns församling
Augusti 2015 - Juli 2018

### Kurser inom mat och dryck : 30hp
Umeå Universitet
Januari 2023 - Januari 2025
- Vinkunskap i teori och praktik 
- Vinkunskap: Fördjupning 
- Ölkunskap i teori och praktik
- Drycker och mat i kombination

## Arbetslivserfarenhet
Sedan 2015 har jag provat på lite allt möjligt för att tjäna några extra slantar men också för att samla på mig erfarenheter och utvecklas. 
Nedan följer ett noggrant urval av roller jag haft.

### Lilla Krogen : Servis
Öst på stan, Umeå
Juli 2026 - NU
Jag tog chansen att hjälpa Lilla Krogen när de behövde personal för ett bröllopsuppdrag i slutet av juli 2026 och en månad senare behövde de fylla på personalstyrkan i deras matsal och då hörde jag snabbt av mig och fick en tjänst direkt. Denna roll liknar inget av mina tidigare restaurangjobb eftersom det är högre klass på alla plan samt mycket större personligt ansvar då vi ofta bara är två som jobbar under öppettiderna. Restaurangen får ofta beröm och hyllas för att servera Umeås bästa mat och min roll i maskineriet är att vägleda gästerna från att de kommer in i dörren, genom att de får sin goda mat framför sig, till att de går ut genom dörren med tanken att "Wow, hit måste vi gå igen". 

### Droskan Pub och Restaurang : Bartender
Öst på stan, Umeå
Juli 2021 - NU
Från att ha mat, dryck och krogkultur som ett sidointresse fick jag möjligheten att komma in och hjälpa till hos Droskan när de behövde personal. Nästan direkt fick jag börja jobba i baren och allt eftersom fick jag mer och mer ansvar. Under sommaren 2023 höll jag och en kollega musikquiz en kväll i veckan och jag fick dessutom sköta hemsidan under sommaren. Under 2024 och delar av 2025 var jag barchef och sortimentsansvarig men klev av rollen för att fokusera på mina studier. Jag jobbar fortfarande ibland åt Droskan, framför allt på evenemang där gästerna/publiken ser det som en självklarhet att se mig i baren. När det kommer till sysslor man kan göra som anställd i krogbranschen har jag nog lyckats göra i princip allt på Droskan: Bar, servis, hovmästare, festbokare, ekonomi, lager, diskare, runner, garderob, kock, DJ, musiker, ljud- och ljustekniker, städare, programmerare.

### ICA Nära Västerslätt : Vikarie färskvaror
Västerslätt, Umeå
Sommaren 2025 och 2026
Ett sommarjobb som jag tog på mig för lite omväxling efter flera somrar i restaurang. Det hjälpte mig att utveckla min känsla för service på ett annat sätt och jag fick även mer kunskap om livsmedelshantering och lagerhållning. 

### Umeå Universitet : Amanuens/Handledare
Umeå Universitet
Oktober 2023 - Januari 2026
Under HT23 var jag handledare för kursen "Programmeringsteknik med C och Matlab", där jag hjälpte studenter under handledningstillfällen och ledde lektioner med kodgranskning. Mitt fokus var att lära ut pedagogiskt så att studenterna kunde lösa problem självständigt efter att ha fått hjälp
Under HT24 och HT25 var jag amanuens på kursen "Datakommunikation och Internet", där jag ansvarar för en modul där studenterna programmerar en webbserver. Jag har hållit lektioner, handlett studenter och bedömt både kodinlämningar och redovisningar. Rollen har gett mig mer ansvar och möjlighet att utveckla både kursen och mina pedagogiska färdigheter vilket jag har tyckt varit väldigt intressant, spännande och givande.
Under VT25 var jag amanuens på kurserna “Datastrukturer och Algoritmer (Python)” och “Objektorienterad Programmering (Java)”. I dessa kurser fick jag förutom att handleda studenterna även bedöma labbrapporter och ge feedback på studenternas systemdesigner.
Jag valde att bli handledare/amanuens för att jag gillar att lära ut och har en bakgrund som ledare i kyrkan.

### Restaurang Båten : Bartender
Umeälven, Umeå
Sommaren 2024
Efter att ha jobbat två somrar som bartender på Droskan ville jag prova jobba på något annat ställe och valde Båten eftersom det var mitt favoritställe att själv besöka. Fick lära mig mer om hur man kan jobba i restaurang när man har ett lite större arbetslag samt hur man kastar ut drinkar i högt tempo under nattklubbar. 

</div>
<div><div style="width: 100%; display: flex; justify-content: center; align-items: center;"><img src="https://im16.inviewer.se/skiss/56/56ME4AMDWG.jpg" alt="Bild på mig :)" style="object-fit: cover; height: 200px; width: 400px; border-radius: 0%"></div><div id="cv-right" class="cv-column language-markdown">## Kontaktuppgifter
Rallarrosgränd 38
Umeå 90353
073 020 46 96
jfkgustav@gmail.com
född 2000-02-02
[Hemsida/Portfolio](https://gustavjohansson.netlify.app)

## Projekt
Nedan följer några utvalda projekt som jag varit en del av. Besök gärna min [GitHub](https://github.com/jfkgustav/) för att se fler projekt jag jobbat på :)

### BuildYourSetlist
Första release: Augusti 2026
Stack: Svelte + SvelteKit + Tailwind + Supabase
Länk: [BuildYourSetlist](https://buildyoursetlist.netlify.app/)
Detta projekt löser ett problem som jag själv stöter på rätt ofta. Jag är musiker och inför varje konsert får man alltid en tidsram att hålla sig till. Det kan vara allt från 15 minuter till 3 timmar. Oavsett vad kan det vara svårt att på förhand uppskatta hur många låtar man hinner med på den utsagda tiden, eftersom låtar kan vara så olika långa. Därför har jag länge drömt om att skapa en lösning till detta och under sommaren 2026 kom jag till skott. Med BuildYourSetlist kan man enkelt skapa en "låtbank" genom att importera låtar/låtlistor från Spotify, Google Drive eller CSV-filer och därefter bygga setlists utifrån en given tidsram. Nuvarande versionen löser problemet hyfsat bra men saknar några önskvärda funktioner som exempel mobilstöd, dataanalys/statistik och önske-läge, där man vänder på konceptet och låter publiken önska låtar utifrån din låtbank (perfekt för trubadurer!).

### RadioInfo
Första release: Januari 2025
Stack: Java + Swing
API: Sveriges Radios öppna API
Länk: [Körbar JAR-fil](https://gustavjohansson.netlify.app/RadioInfo.jar)
Som en del av kursen "Applikationsutveckling i Java" gjordes "RadioInfo", Ett program som kan visa programtablån för olika kanaler från Sveriges Radio.

### MS Röj-klon
Första release: November 2024
Stack: Java + Swing
Länk: [Körbar JAR-fil](https://gustavjohansson.netlify.app/minesweeper.jar)
En egen utmaning att göra en enkel version av spelet "Minesweeper"/"Röj" på en förmiddag för att lära mig grunderna för att skapa GUI med Javas Swing-bibliotek.

### skrivert
Våren 2024
Verktyg: Figma + Svelte + ShadCN + Tailwind
Länk: [En bild från GUI:t](https://gustavjohansson.netlify.app/_app/immutable/assets/settings.DrpOaWvy.png)
Ett projekt under kursen "Design-Build-Test" där vi skapade GUI till ett textproduktionsprogram.

### 3D Studio
Första release: December 2023
Stack: C++ + OpenGL + GLM + tinyOBJloader 
Länk: [GitHub-repo](https://github.com/jfkgustav/3dstudio)
Simpel grafikmotor skriven i C++ som del av kursen "Datorgrafik".

### Thatchers hemsida
Första release: April 2024
Stack: Svelte + SvelteKit
Länk: [Thatchers Hemsida](https://thatchers.netlify.app/)
Mitt första band Thatchers hemsida där man kan hitta vår musik, bilder och filmer på oss samt på ett väldigt enkelt sätt boka/beställa merch.

## Färdigheter
B-körkort
Serveringsvana
Kassavana
Kassaredovisning
Fakturahantering
Datorvana - Word, Excel, Powerpoint och Adobe-sviten
Go, React, Svelte, SQL, C, C++, C#, Java, Python, Matlab, R, .NET, HTML, CSS, JavaScript, TypeScript 

> Referenser lämnas på begäran.
</div>
					</div>
				</div>
			</div>
		</main>

		<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.10.0/highlight.min.js"></script>
		<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.10.0/languages/markdown.min.js"></script>


 <script>
  (() => {
    document.querySelectorAll(".cv-column").forEach((column) => {
      let markdown = column.textContent
        .replace(/\r\n?/g, "\n")
        .trim();

      const lines = markdown.split("\n");
      const indents = lines
        .filter(line => line.trim().length > 0)
        .map(line => line.match(/^\s*/)[0].length);

      const minIndent = indents.length
        ? Math.min(...indents)
        : 0;

      markdown = lines
        .map(line => line.slice(minIndent))
        .join("\n");

      const highlighted = window.hljs.highlight(markdown, {
        language: "markdown"
      });

      column.innerHTML = highlighted.value;
      column.classList.add("hljs");

      // Gör länkar klickbara utan att ändra Highlight.js HTML.
      const anchors = [];
      const walker = document.createTreeWalker(
        column,
        NodeFilter.SHOW_TEXT
      );

      const nodes = [];
      while (walker.nextNode()) nodes.push(walker.currentNode);

      nodes.forEach((node) => {
        const text = node.nodeValue || "";
        const match = text.match(/^https?:\/\/\S+$/);
        if (!match) return;

        const a = document.createElement("a");
        a.href = text;
        a.target = "_blank";
        a.rel = "noopener noreferrer";
        a.className = "md-link";
        a.textContent = text;

        node.parentNode.replaceChild(a, node);
      });
    });
  })();
</script>
	</body>


