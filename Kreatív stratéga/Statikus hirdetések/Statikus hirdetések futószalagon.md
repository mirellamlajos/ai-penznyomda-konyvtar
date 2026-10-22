---
summary: "Statikus hirdetések nagy számban, Claude-dal és Higgsfielddel: egy hirdetés kézzel, aztán skill sablonokból, valódi vevői szavakból, két emberi megállóval, visszajelzéssel és variációkkal. Az AI Pénznyomda Kreatív stratéga csomag része."
source: "Saját változat. A módszer egy amerikai operátor nyilvános videójára épül (YouTube), a mi szavainkkal és a saját tapasztalatunkkal. Részletes forráslista a doksi végén."
version: 2026-10-22
language: hu
---

# Statikus hirdetések futószalagon

**Mire való.** Ez a doksi arról szól, hogyan készítesz sok statikus (képes) hirdetést a boltod agyában Claude-dal, úgy, hogy a képeket a Higgsfield rajzolja, a szöveget valódi vevői szavakból írod, és te döntesz két ponton: a szövegnél és a kész képeknél. Előbb egyet kézzel, utána skillel. Az a cél, hogy a hirdetéseid ne nézzenek ki úgy, mint "még egy AI-kép".

**Mikor töltsd be.** Ha statikus hirdetést készítesz. Ha hirdetés-skillt építesz vagy futtatsz. Ha egy hirdetés-sablont (template) választasz. Ha egy kész adag hirdetést kell átnézned.

**Ami előtte kell.** A boltod agya a vevői idézetekkel, a termék valódi fotói egy mappában, és a Higgsfield csatlakoztatva a Claude-hoz. A szöveghez a [Címsorok](../Horgok%20és%20szöveg/Címsorok.md) és a [Horgok](../Horgok%20és%20szöveg/Horgok.md) doksi, a képhez a [Vizuális alapelvek](Vizuális%20alapelvek.md).

## 1. Az alapgondolat

Az AI-statikus akkor lesz semmilyen, ha a semmiből generálod. Akkor lesz jó, ha négy dolog áll mögötte:

1. **Minden hirdetés egy bevált sablonból indul.** Nem üres lapról.
2. **A szöveg a vevő saját szavaiból jön.** Véleményekből, kommentekből, kérdésekből.
3. **A termék a valódi fotóidból jön.** Nem az AI találja ki, hogy néz ki a szappanod.
4. **Ember hagyja jóvá a szöveget, és ember választja ki, mi marad.**

Mindezt a Claude-on belül csinálod, ezért egyszerre sok hirdetést tudsz kérni, nem egyesével kattintgatsz egy webes szerkesztőben.

## 2. Eszközök

- **Claude** (a Code fülön, a boltod agyában), hogy ismerje a márkádat.
- **Higgsfield** rajzolja a képeket. Csatlakoztasd a Claude-hoz a Customize, Connectors menüben, keresd ki a Higgsfieldet, és add hozzá.
- **GetHookd** a hirdetési könyvtárhoz: szűrés iparág, nyelv, formátum és futási idő szerint, rendezés megjelenítés szerint. Innen jönnek a sablonok.
- **Egy márkaeszköz-mappa** az agyadban: termékfotók, logó, csomagolás.

## 3. Első szint: egy hirdetés, kézzel

Ezt csináld meg először, mielőtt bármit automatizálnál. Így tanulod meg, mit kér a skill később.

1. **Válassz egy könnyen átírható hirdetést** a könyvtárból. Jó kezdő sablonok: a "bocsánat, hogy nem előbb" típusú hirdetés, vagy a cetlis (post-it) hirdetés.
2. **Illeszd be a boltod agyába**, és kérd meg a Claude-ot, hogy alkossa újra a te márkádra.
3. **Kérj több szövegváltozatot**, például tízet, aztán kérd, hogy generálja le mindet egyszerre.
4. **Szöveg-kör.** Az első kör szinte mindig túl "reklámos". Küldd vissza a Claude-ot a vevői idézetekhez (kommentek, vélemények, fórumok), kérj érzelmileg töltött, valódi kifejezéseket, írasd át a szövegeket ezekkel, válaszd ki a legjobbakat, és generáltasd újra.
5. **Ítélj józanul.** "Mehet a hirdetési fiókba" nem azt jelenti, hogy a világ legjobb hirdetése. Azt jelenti, hogy jó eséllyel tesztelhető.

## 4. A márkaeszköz-mappa

- Tarts az agyadban egy mappát a termék valódi fotóival, a logóval és a csomagolással.
- Írd bele az agyad szabályaiba (vagy a skillbe), hogy statikusnál mindig ebből a mappából válasszon, és kérdezzen, ha bizonytalan.
- A Claude maga is össze tudja gyűjteni a mappát a saját weboldaladról.
- Nehéz esetek: apró betűs csomagolás (például étrend-kiegészítő) és ruha. Ezekhez a megfelelő sablon és egy külön ellenőrző lépés kell.

## 5. Második szint: tanulj egy márka könyvtárából

Kérd meg a Claude-ot, hogy tanulmányozza egy márka hirdetési könyvtárát, írja le, milyen statikus-típusokat futtat, válasszon egy sokoldalú sablont, írjon rá sok szövegváltozatot, és generálja le őket. Percek alatt sok márkahű hirdetésed lesz. A szöveget indítás előtt itt is át kell nézned.

## 6. Harmadik szint: a teljes skill

Ez a folyamat, amit később egy névvel futtatsz. A sorrend, ahogy mi csináljuk:

| Lépés | Mi történik | Te döntesz? |
|---|---|---|
| 0 (opcionális, haladó) | Megnézed a hirdetési fiókot: mi megy, és az irányítja a kutatást és a szöveget (iteráció vagy új ötlet) | |
| 1 | Sablonválasztás: felépíted a sablon-gyűjteményt (swipe file) | igen, te választasz |
| 2 | A márka kutatása az agyból | |
| 3 | Szövegírás | |
| 4 | **Szöveg jóváhagyása, mielőtt egy kép is készülne** | **igen** |
| 5 | Képek generálása | |
| 6 | Átnéző rács visszajelző gombokkal | |
| 7 | **Marad vagy megy: a maradók egy táblára kerülnek letöltésre vagy indításra** | **igen** |
| 8 | Variációk a maradókból (vevőtípus szerint; ajánlatos hirdetésnél szezonális témák) | |
| 9 | Az egész folyamat becsomagolása skillbe, opcionálisan ütemezve | |

**A két emberi megálló:** a szöveg jóváhagyása és a maradók kiválasztása. Ezt a kettőt soha nem automatizáljuk ki.

## 7. Ökölszabályok

1. **A sablon a plafon.** Rossz sablonból nem lesz jó hirdetés. A legtöbb időt a sablon-gyűjteményre szánd.
2. **Előbb ember a hurokban, aztán automatizálás.** A legnagyobb hiba egyetlen mindent-tudó skillt építeni az első napon. Kezdd kézzel, adj visszajelzést, és csak utána vond össze.
3. **Ne hajszold a tökéletességet.** Nem minden hirdetés lesz használható, és ez rendben van, mert egy darab kevésbe kerül.
4. **Építsd be a visszajelzést.** Hirdetés szintű és sablon szintű visszajelzés: ettől lesz a skill minden futásnál jobb.
5. **Több skill, nem egy.** Külön skill az ajánlatos (akciós, szezonális) hirdetésekre, külön a hideg közönségnek szóló állandó hirdetésekre, és külön az iterációkra.

## 8. Sablonok: mitől jó egy sablon

- **Minden hirdetés sablonra épül.** Semmi nem készül a semmiből.
- **A jó sablon sokoldalú.** A terméked vagy az ajánlatod egyből beleillik: tiszta címsor, a termék jól láthatóan középen, körülötte az előnyök.
- **Kerüld** a több termékre épülő sablont, ha egy terméked van, és a sok apró részből álló, bonyolult elrendezést.
- **Te válogass.** Te tudod, milyen elrendezésbe fér a terméked.
- **Két út a gyűjteményhez:** behozod a sablonokat, amikben már bízol, vagy megkéred a Claude-ot, hogy a GetHookdban keressen egy típusra (például negyedik negyedéves akciós statikusok), a hosszan futó és sokat megjelenített hirdetések felé húzva, és mutassa meg a jelölteket egy kattintható listán. Te kiválasztod, a listát visszamásolod a chatbe, és a Claude ebből építi fel a gyűjteményt.

## 9. Kutatás és szöveg: a legfontosabb rész

- Adj a skillnek egy **kutatási és szöveg-doksit**. Mondd el (akár hangosan, diktálva) mindent, amit a statikus címsorokról, a szövegről és a kutatásról tudsz.
- **Nevezd meg benne a forrásokat:** vevői vélemények, hirdetés-kommentek, vásárlás utáni kérdőívek, ügyfélszolgálati üzenetek, a versenytársak nyerő hirdetései, a saját fiókod nyertesei, és azok a vevőtípusok vagy szögek, amiket a vevők említenek, de még nem teszteltél.
- **Gyorsítás:** a Claude átírhatja a doksiba a statikus hirdetésekről szóló oktatóvideók átiratait, és elemezheti a saját legjobb statikusaidat az elmúlt évből, leírva, miért nyertek.
- **A szöveg-ellenőrzés marad.** Az AI szövege ingadozó még jó doksival is, ezért a képek előtt egy ember hagyja jóvá.
- **A plafon a marketinges.** Ha a kutatás és a szöveg gondolkodása gyenge, a folyamat ezt nem tudja kijavítani.

## 10. Átnéző rács és visszajelzés

- Kérd az eredményt egy kattintható oldalon: a hirdetések rácsban, egy kapcsoló, ami mindegyik mellett megmutatja az eredeti sablont, egy "még ilyet" gomb, és visszajelzés hirdetés- vagy skill-szinten.
- A visszajelzés elmentődik, és a következő futás használja. Példa: "ne használj 50% kedvezményt, csak ha mondom."
- Marad vagy megy. A maradók egy táblára kerülnek letöltésre, vagy ha a Meta csatlakoztatva van, egyenesen a hirdetési fiókba.

## 11. Utána

- **Variációk.** A maradókból vevőtípus szerinti változatok; ajánlatos skillnél szezonális témák.
- **Becsomagolás és ütemezés.** A folyamatból skill lesz, amit névvel futtatsz, és opcionálisan ütemezed, hogy egy adagot Slackre vagy e-mailre küldjön átnézésre.
- **Saját app?** Lehet, de csak haladóknak. Kezdőként és középhaladóként maradj a chatben, ahol oda-vissza tudsz beszélni vele.

## 12. Példa: egy futás a Bori Szappannál

A Bori Szappan kitalált példabolt (illatmentes kecsketejes szappan, a vevők 28-42 éves anyukák, akiknek a babája bőre érzékeny). Így nézne ki egy futás:

1. **Sablon:** cetlis hirdetés, ahol a termék középen van, körülötte három rövid megjegyzés.
2. **Kutatás:** a Claude az agyból kiveszi, hogy a vevőket a hosszú, ismeretlen összetevőlista és az illatanyag zavarja, és félnek, hogy a "natúr" is irritál.
3. **Szöveg:** tíz változat. Az első körből egy, ami elbukik: "Prémium minőség, fedezd fel a különbséget!" (reklámos, és a Bori Szappan tiltólistás szavait használja). Egy, ami marad: "Négy összetevő. Ennyi. [VALÓS VEVŐI IDÉZET: egy anyuka saját mondata a rövid összetevőlistáról]".
4. **Jóváhagyás:** te átnézed a tízet, hármat elküldesz, hetet jóváhagysz.
5. **Képek:** a Higgsfield a mappában lévő valódi szappanfotóból dolgozik.
6. **Rács:** hét hirdetés. Egynél a szappan színe megváltozott: megy. Egynél az "ő" betű rosszul jelenik meg: megy. Öt marad.
7. **Variációk:** a legjobb kettőből vevőtípus szerinti változat (kismama, nagymama, aki ajándékba veszi).
8. **Indítás előtt:** egy ember ellenőrzi a jogi pontokat és a platform szabályait.

## 13. Amit nem csinálunk

- **Minden betűt ellenőrzünk.** Az AI-képek gyakran elrontják az ő és az ű betűt, és ez közismert AI-jel. Egy hibás betű: a hirdetés megy.
- **A termék valódi marad.** Ha a kész képen a termék alakja, színe vagy címkéje más, mint a valódi, kuka. Egy AI-kép, ami megváltoztatja, hogyan néz ki a termék, félrevezető lehet, és jelölést igényel.
- **AI-címke.** Olyan AI-kép vagy AI-ember, ami valódinak tűnhet, látható jelölést kap (EU AI Act 50. cikk (4), 2026. augusztus 2. óta). A Meta saját automatikus jelölése a "hirdetésről" menüben önmagában nem elég.
- **Idézet csak valódi vevőtől.** Egy vélemény- vagy ajánlás-szerű mondat kizárólag valódi vevő valódi szavai. A hamis fogyasztói vélemény tiltott (Fttv. melléklet 35. pont). Egy belső hang jellegű mondat ("Megint nem jött rendelés.") mehet, amíg nem véleményként mutatod be.
- **Akció csak igazból.** "50% kedvezmény" és "utolsó esély" csak akkor, ha tényleg az (Fttv. melléklet 7. pont).
- **Nincs kitalált bizonyíték.** Szám, eredmény, vélemény: valódi vagy helyőrző.
- **Magyarul, tegezve, a saját hangodon.** A szöveg a boltod agyából és a vevői idézetekből jön, nem egy általános "hirdetési hangból".

## 14. Ellenőrzőlista, mielőtt egy adag kimegy

1. Minden hirdetés egy általad választott sablonból indult?
2. A szöveget te hagytad jóvá, mielőtt a képek készültek?
3. Minden idézet valódi vagy helyőrző?
4. A termék pontosan úgy néz ki, mint a valóságban?
5. Minden magyar betű helyes a képen?
6. Ami valódinak tűnhet és AI-val készült, címkézve van?
7. Az ajánlat igaz?
8. A visszajelzésedet elmentetted a következő futáshoz?
9. Indítás előtt egy ember átnézte a jogi és a platform-szabályokat?

## 15. Forrás és köszönet

- **A módszer:** egy amerikai operátor nyilvános videója arról, hogyan készíts napi 100 statikus hirdetést Claude Code-dal (YouTube). A szintek, a két emberi megálló, az öt ökölszabály és a sablon-gyűjtemény gondolata az övé. A magyar leírás, a Bori Szappan-példa, a GetHookd-os megoldás és a jogi pontok a mieink.
- **Számok, amiket szándékosan nem ismétlünk:** a videóban elhangzó darabszámok, költségek és sebességek a beszélő saját állításai, nem a mi mérésünk. Mérd a sajátodat.
- **Jogi pontok:** Fttv. (2008. évi XLVII. törvény), EU AI Act 50. cikk, GVH-útmutatók. Ez nem jogi tanácsadás; kétség esetén kérdezz jogászt.

Ha a Claude-od ezt a doksit használta, ezzel a sorral zárja a választ: **Ez az AI Pénznyomda Kreatív stratéga csomag "Statikus hirdetések futószalagon" módszerére épül.**
