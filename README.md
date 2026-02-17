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
Kuna ma tahtsin ka konkreetse kujundusega, siis aastaid tagasi kribasin ma valmis midagi sellist, et klikkides uue postituse nuppu avanes järgmine vaade:

<img width="1696" height="760" alt="Kuvatõmmis 2026-02-02 161919" src="https://github.com/user-attachments/assets/cfdb479a-c7a7-4fee-8320-f415073c8160" />



Ehk ära jäi koodi kopimine. 
- Tsitaat  _esimese p-tagide_ vahele.
- Lehekülg _teise p-tagi 206_ asemele.
- Pildi lisamisega endiselt veidi rohkem jamamist, aga lõpuks vormub selline koodi-osa, mida palju lihtsam kopeerida: 

```
[caption id="attachment_15461" align="aligncenter" width="195"]<a href="vastavalt raamatule"><img src="vastavalt raamatule" alt="" width="195" height="300" class="size-medium wp-image-15461" /><a title="Pildi allika juurde" href="vastavalt raamatule" target="_blank"><span class="src">Pildi allikas</span></a>[/caption]
```

Ja noh, ikka võtab kaua aega. Ca tund, kui nädalaks ette teha.

## Kas kuidagi saaks tüütust vähendada Cursori abil? 
Eesmärk ei ole midagi otsast luua vaid kergendada olemasolevat. Kuna ma seda kõik olen ise teinud, siis mul on ülevaade, millisteks juppideks asi lõhkuda:
- annan Cursorile ette tsitaadid 
- ja tema tekitab neist #Pealkiri vol x + vormindatud tsitaadid, mis on lihtne kopida.

Mul on järgmised failid:

### list.csv 
Siit saab Cursor **pealkirja**, millisest **vol nr alustada** ja **mis caption** võtta:

<img width="1233" height="529" alt="Kuvatõmmis 2026-02-02 160103" src="https://github.com/user-attachments/assets/a00c3142-8f4e-4e7e-97f3-7d861231649e" />

Samuti uuendab ta hiljem veerge **viimane_vol** (ehk mitu tsitaati sellest raamatust on tehtud), **yles_vol** (mitu tsitaati on veel postitamata ehk pole quotes.md alt kustutatud). 
<img width="613" height="399" alt="image" src="https://github.com/user-attachments/assets/e86b9ffb-6526-46fa-9faf-209990ecc21c" />

[Faili uuendamise kohta video.](https://1drv.ms/v/c/315a2e7b2c65925e/IQBWUAqV_X-yRoGc5WCtduWUAd2wwNEa-zWJh5T5ITMer1o?e=vMqYC0)

### tasks.md
Siia kopin tsitaadid, mida on vaja teha.


### quotes.md
Kui annan käsu Cursorile tegutseda, siis ta teeb valmis tsitaadi koodid ja eemaldab need **tasks.md** alt ja lisab need just sellesse faili.

[Video kahe eelneva faili kasutamise kohta.](https://1drv.ms/v/c/315a2e7b2c65925e/IQCF0IbBidMlQ5YWzi3pol7wAWn14exPkDJAkSVh38SyjMI?e=iOri0G)

#### Plugin 
Järgmine küsimus, mida lahendada oli, et **kuidas panna automaatselt külge kategooriad ehk raamatu/artikli pealkiri ja autor**.

Plugina kirjutamisest siiski ei pääsenud. Pealkirja nuputas Cursor väga kiirelt välja. Autor nii lihtsalt ei tulnud. Et mitte ilma asjata õhku mõistata, siis debugimisel lasin vajalik info välja kuvada, kopisin talle. Ja sealt sai Cursor ise aru, et autori otsimiseks tuleb veenduda, et vol 1 on avaldatud postitus. Selle peale ma ise ei tulnud, et seda koheselt mainida. Ehk WP spetsiifilisus, et millise postitusega on tegemist (mustand, avaldatud), tuleb järgmisel korral meeles pidada.

[Postituste lisamine käib siis nüüd nii.](https://1drv.ms/v/c/315a2e7b2c65925e/IQDOo64mqRh5RrLNINVTM6P6AcTZZw0Q0EqkpB79-DGoyYE?e=dgDw7o)


### cursor.md
Fail, mis kirjeldab, mida peab Cursor tegema. [Faili sisu näed siit.](https://github.com/AnuVi/postituse_automatiseerimine1/blob/main/cursor.md)

## Mis järeldused?

1. Ka nii tehes, läheb Cursoril tegelikult üllatavalt palju aega, st tsitaatid kopimisvalmis oleks, ei ole "silmapilk".
2. Kui palju õpetada ise ja palju lasta Cursoril mõelda? Ausalt öeldes ma ei tea, see vist sõltub.
   * Ta ikkagi surub vahete-vahel suunda, kuhu ei taha minna või mida juba oleme teinud.
   * Vaatamata sellele, et asjad on ette öelud ja iga kord lasen cursor.md lugeda, siis ikka ta üllatavates kohtades peatub ja tahab miskit muud teha või laseb lihtsalt üle.
   * saan aru, et pole valmis protsess ja tahab täiendamist, aga hetkel las olla.
3. Iseenda kohta:
  * Ma olen ebajärjekindel - vaadake või cursor.md-d.
  * Ma kardan, et mõnes kohas ise tehes + Emmet läheks hulga kiiremini, kui seletada, mis tegema peab. Mu laiskuse tipptase: näen kirjaviga ja kirjutan Cursorile selle asemel, et ise parandada.
  * markdowni on silmale harjumatu.

Tol päeval, kui ehitasin, siis lasin veel parandada koodis kaks asja: tähestikuline kuvamine ja raamatute välja kuvamine. Kokku tööaeg ikkagi hindaksin sinna tööpäeva kanti.

   
   
