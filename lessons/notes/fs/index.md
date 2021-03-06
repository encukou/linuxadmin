# Souborové systémy – mini úvod

Pojďme si přiblížit, jakým způsobem Linux zapisuje informace – soubory
a adresáře – na disk.

## Archivy

Jak fungují archivy?

Představ si knížku. Knížka je v podstatě sekvence písmenek.
Když se chceš podívat na určité místo, nemusíš listovat každou stránku zvlášť.
Pro vyřešení tohoto úkolu najdeš prvně v knížce **Obsah**, který řekne například: *tato kapitola je na stránce 254*.
Podobně je vše na disku uloženo jako sekvence bajtů.
To, že jsou v něm nějaké soubory a adresáře, o nichž jsme se minule bavili, je jen iluze.
Ve skutečnosti je na disku jedna dlouhá sekvence jedniček a nul.
V tom by se ale vyhledávalo špatně, a proto má počítač v rámci svých jedniček a nul speciální informace, které podobně jako obsah v knížce říkají: *zde jsou adresáře, v nich jsou tyto soubory, jsou takto velké, takto se jmenují* atd.

Nejlepší si to bude ukázat na příkladu archivu `zip`. 


### ZIP

- https://commons.wikimedia.org/wiki/File:ZIP-64_Internal_Layout.svg

Obsahuje jednu dlouhou sekvenci informaci, na jejíž konci je *centrální adresář*. Ještě za ním je informace o počtu souborů v archivu.
V centrálním adresáři je řečeno: *1. soubor začíná na 0. pozici, 2. soubor začíná na 15. pozici* atd. 
Jsou v něm také informace o jednotlivých souborech: mj. jejich jména a jak jsou dlouhé.

> [note]
> Centrální adresář se nachází v zipu na konci, což má svůj důvod.
> Můžeš vzít normální soubor, na konec mu přilepit `zip`, a soubor bude pořád
> fungovat i jako starý soubor – pokud ho čteš jen od začátku do původního
> konce souboru.

Soubory v zipu se dají docela jednoduše číst.
Podíváš se, kde začít a jak dlouho číst, a je to.


## Souborový systém

Podobně jako archiv Zip fungují *souborové systémy* – způsob,
jak ukládat a spravovat spoustu souborů a adresářů na disku.
Na určitých částech disku jsou uložena data jednotlivých souborů;
na jiných je uložen seznam souborů v adresářích;
jinde jsou popisy souborů obsahující informace o jejich vlastnostech.

Na rozdíl od zipu je „opravdový“ souborový systém složitější – například
„adresář“ není centrální, ale bývá pro každou složku zvlášť.
„Opravdový“ souborový systém je dělaný nejen na čtení souborů,
ale i na snadný zápis.
(To teoreticky jde i v zipu, ale problém vzniká, pokud soubor, který
chceš do archivu nahrát, je větší než místo, které je v něm k dispozici.)

Základní myšlenka ale zůstává stejná.
