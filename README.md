## Algus
Pean aastaid üht lugemisblogi, kuhu talletan loetuid tsitaate. Avaldamisele tuleb üks tsitaat korraga.
Alguses põnev, aga mingi hetk läks jube tüütuks:

1. Pealkiri: lisada või linnutada **Raamatu/Artikli kategooria** all.
2. Autor: lisada või linnutada **Autori kategooria** all.
3. Siis teha postitus:
  - Pealkiri vol.
  - Tsitaat.
  - Lehekülg.
  - Pilt lisada või üles otsida Internetist.
  - _Tag_ külge panna.
  - Avaldada või seadistada avaldamine.

## Koodi kopimise vältimine
Kuna ma tahtsin ka konkreetse kujundusega, siis aastaid tagasi kribasin ma valmis midagi sellist, et klikkides uus postitus nuppu avanes järgmine vaade:

<img width="1303" height="480" alt="Kuvatõmmis 2026-02-02 134823" src="https://github.com/user-attachments/assets/2349b694-eeb8-4e4c-a04e-5c84927be344" />


Ehk ära jäi koodi kopimine. 
- Tsitaat  _esimese <p>-tagide_ vahele.
- Lehekülg _teise <p>-tagi 206_ asemele.
- Pildi lisamisega endiselt veidi rohkem jamamist, aga lõpuks vormub selline koodi-osa, mida palju lihtsam kopeerida: 

```
[caption id="attachment_15461" align="aligncenter" width="195"]<a href="vastavalt raamatule"><img src="vastavalt raamatule" alt="" width="195" height="300" class="size-medium wp-image-15461" /><a title="Pildi allika juurde" href="vastavalt raamatule" target="_blank"><span class="src">Pildi allikas</span></a>[/caption]
```

Ja noh, ikka võtab kaua aega. Ca tund, kui nädalaks ette teha.

## Kas kuidagi saaks tüütust vähendada Cursori abil? 
Eesmärk ei ole midagi otsast luua vaid kergendada olemasolevat. Kuna ma seda kõik olen ise teinud, siis mul on ülevaade, millisteks juppideks asi lõhkuda:
- annan Cursorile ette tsitaadid 
- ja tema tekitab neist #Pealkiri vol x + vormindatud tsitaadid, mis on lihtne kopida.

Protsess lähemalt
Mul on 
### list.csv 
Siit saab Cursor pealkirja, millisest vol nr alustada ja mis caption võtta:

<img width="1233" height="529" alt="Kuvatõmmis 2026-02-02 160103" src="https://github.com/user-attachments/assets/a00c3142-8f4e-4e7e-97f3-7d861231649e" />

