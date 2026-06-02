## Uživatelské role v systému


* **Neregistrovaný uživatel (Divák):** Tato role slouží k pasivnímu prohlížení veřejného obsahu. Umožňuje uživateli vidět hlavní sociální feed a celkové žebříčky úspěšnosti, ale neopravňuje ho k žádným aktivním akcím, jako je zápis výsledků nebo komentování.

* **Registrovaný hráč (Student):** Základní uživatelská role pro každého spolužáka. Tato role umožňuje vytvářet osobní profil, zakládat zápisy o odehraných hrách, schvalovat výsledky zápasů, psát komentáře a udělovat reakce na hlavní nástěnce.

* **Kapitán týmu (Zástupce třídy):** Rozšířená role pro zakladatele konkrétního herního týmu. Dává uživateli právo spravovat soupisku (přidávat nebo odebírat spoluhráče ze třídy) a měnit veřejné informace o týmu, například jeho název nebo týmové logo.

* **Administrátor (Správce systému):** Nejvyšší role s plným přístupem k řízení aplikace. Slouží k moderování komunitního obsahu (mazání nevhodných komentářů), řešení sporů u neshodných výsledků, správě uživatelských účtů a případnému blokování podvodných profilů.

## 1. Funkční požadavky


* **F01 - Registrace přes školní účet:** Funkce ověřuje e-mailovou doménu při registraci a dovoluje vytvoření účtu pouze uživatelům s adresou @pslib.cz, čímž zajišťuje bezpečnost a uzavřenost komunity.

* **F02 - Správa osobního profilu:** Umožňuje uživatelům nastavit si unikátní přezdívku, nahrát profilový obrázek a zvolit svou domovskou třídu, což slouží ke správné identifikaci v žebříčcích.

* **F03 - Tvorba a správa týmů:** Dovoluje hráčům ze stejné třídy vytvářet soutěžní dvojice nebo týmy, které pak společně sbírají body do celkového školního hodnocení.

* **F04 - Záznam odehraného zápasu:** Slouží k zadání výsledků bezprostředně po dohrání hry. Uživatel zde vyplní finální skóre, délku trvání zápasu a vybere ze seznamu konkrétní hráče, kteří se hry účastnili.

* **F05 - Dvoufázové ověření výsledku:** Mechanismus, který po zadání zápasu jedním týmem vygeneruje požadavek na potvrzení pro tým soupeře. Zápas se započítá do statistik až ve chvíli, kdy obě strany s výsledkem souhlasí, což efektivně brání podvodům.

* **F06 - Sociální feed zápasů:** Hlavní přehledová zeď aplikace, která chronologicky řadí a zobrazuje nově ověřené zápasy, takže celá škola okamžitě vidí, kdo zrovna vyhrál.

* **F07 - Komunitní interakce:** Umožňuje uživatelům vyjadřovat emoce pod jednotlivými zápasy ve feedu pomocí předdefinovaných emotikonů (např. oheň, palec nahoru) a psát textové komentáře.

* **F08 - Automatické generování žebříčků:** Funkce na pozadí neustále přepočítává úspěšnost a filtruje výsledky do přehledných tabulek podle nejlepších jednotlivců, týmů i úspěšnosti celých tříd.

* **F09 - Systém herních výzev:** Nová funkce, která umožňuje jednomu týmu oficiálně vyzvat jiný tým přes aplikaci. Soupeři přejde upozornění a mohou se tak předem domluvit na konkrétní velkou přestávku, kdy se zápas odehraje.

* **F10 - Systém achievementů (úspěchů):** Nová motivační funkce, která uživatelům automaticky uděluje virtuální odznaky za herní milníky (např. odznak "Neporazitelný" za 5 výher v řadě nebo "Blesk" za zápas vyhraný do dvou minut).

* **F11 - Notifikační centrum:** Zajišťuje distribuci upozornění v reálném čase. Informuje uživatele, že ho někdo vyzval na zápas, že je potřeba potvrdit výsledek, nebo že někdo okomentoval jeho herní výkon.

* **F12 - Administrátorská konzole:** Speciální rozhraní pro správce, které slouží k rychlému mazání vulgárních komentářů, manuální úpravě chybně zadaných dat a správě uživatelských oprávnění.

## 2. Nefunkční požadavky


* **N01 - Mobilní responzivita:** Vzhledem k tomu, že stolní fotbálek je ve sklepě, aplikace musí být primárně navržena a optimalizována pro displeje mobilních telefonů, aby bylo zadávání dat u stolu pohodlné.

* **N02 - Odezva systému:** Přepočet celkových statistik a aktualizace žebříčků po schválení zápasu nesmí trvat déle než 3 sekundy, aby uživatelé měli okamžitou zpětnou vazbu.

* **N03 - Bezpečné ukládání dat:** Uživatelská hesla nesmí být v databázi uložena v otevřeném textu, ale musí být bezpečně zašifrována pomocí moderních hashovacích algoritmů.

* **N04 - Podpora tmavého režimu (Dark Mode):** Uživatelské rozhraní musí obsahovat tmavé téma, které vizuálně ladí s prostředím školního sklepa a šetří baterii mobilních zařízení.

* **N05 - Spolehlivost a dostupnost:** Informační systém musí vykazovat stabilní dostupnost (uptime) minimálně v době školní výuky a přestávek (každý všední den od 7:00 do 16:00), kdy dochází k největšímu náporu.

* **N06 - Zabezpečení přenosu (HTTPS):** Veškerá komunikace mezi mobilním prohlížečem studenta a serverem musí být šifrována pomocí bezpečnostního protokolu HTTPS, aby nebylo možné data v síti odposlouchávat.