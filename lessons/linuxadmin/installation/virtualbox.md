# Virtuální počítač – instalace VirtualBox

Virtualbox si nejdříve stáhni a nainstaluj z webových stránek https://www.virtualbox.org/wiki/Downloads a postupuj podle pokynů k tvému aktuálně běžícímu operačnímu systému (hostiteli).

Když program spustíš, objeví se grafické okno.
Klikni na tlačitko „Nový“ a pokračuj podle obrázkového návodu:

1. Zadej jméno a typ systému (podle kterého se určuje ikonka).
   „Machine Folder“ nech výchozí (nebo použij jiný adresář);
   nekopíruj ten můj:

  {{ figure(
    img=static('vbox-01.png'),
    alt='Instalace VirtualBoxu – #1',
  ) }}

2. Velikost paměti nastav na 2048 MB (tedy 2GB).
   Pokud je u tebe tahle hodnota v „červeném“ pásmu, použij menší, aby byla
   v zeleném;

  {{ figure(
    img=static('vbox-02.png'),
    alt='Instalace VirtualBoxu – #2',
  ) }}

3. Pevný disk vytvoř nyní:

  {{ figure(
    img=static('vbox-03.png'),
    alt='Instalace VirtualBoxu – #3',
  ) }}

4. Typ souboru a úložiště nech ve výchozích hodnotách:

  {{ figure(
    img=static('vbox-04.png'),
    alt='Instalace VirtualBoxu – #4',
  ) }}

  {{ figure(
    img=static('vbox-05.png'),
    alt='Instalace VirtualBoxu – #5',
  ) }}

5. Velikost souboru zvol 10GB; umístění nech výchozí:

  {{ figure(
    img=static('vbox-07.png'),
    alt='Instalace VirtualBoxu – #7',
  ) }}

6. Po klepnutí na „Vytvořit“ se nový virtuální počítač objeví v seznamu vlevo:

  {{ figure(
    img=static('vbox-08.png'),
    alt='Instalace VirtualBoxu – #8',
  ) }}


7. Tím je virtuální počítač vytvořen.
   Spusť ho zelenou šipečkou „spustit“.
   VirtualBox se zeptá na *obraz disku* ze kterého bude instalovat.
   Vyber *obraz disku*, který sis stáhl{{a}} dříve.

  {{ figure(
    img=static('vbox-insert-dvd.png'),
    alt='Instalace VirtualBoxu – vložení virtuálního DVD',
  ) }}

Virtuální počíteč se teď zapne!
Pokračuj [instalací systému]({{ subpage_url('index#install-system') }}).


{#
XXX: kopírování (sdílená schránka) mezi opravdovým a virtuálním strojem.
   -- static/vbcopyb.jpg
#}

{#
XXX: Bridged network -- see static/bridged-network.png
#}
