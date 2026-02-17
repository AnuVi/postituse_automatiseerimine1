```
<!-- Lisa siia Cursoriga seotud märkmed ja juhised -->
# Cursor
1. Ära kasuta emotikone.
2. Kõik failid, mida lood on väikeste tähtedega ja _alakriipsuga. Ka .md failid.
3. Kood kirjuta juba olemasolevatesse failidesse. Testfaili loomiseks küsi alati luba.
4. Vaata tasks.md, mida on vaja teha, vaata cursor.md kuidas käituda. Lähtu sellest. 
5. Ära dubleeri koodi.
6. Tee ainult tasks.md olevad muudatused.
7.eleta enne, mida plaanid teha ja küsi selleks luba.
8. Kui küsin nõu, anna mulle valikuid, aga kõige lihtsam lahendus anna kõige esimesena.

Kuidas tegutseda:
- kui tasks.md-s on #pealkiri ja sellele järgneb tsitaate kuni /**********/, siis
- list.csv-s vaatad -Tegemata tööd  #pealkiri ja quotes.md-sse tekitad järgmiselt
-- #pealkiri vol #nr
  - kui list.csv veerg #viimane_vol on täidetud, siis liidad +1 sellele
  - kui list.csv veerg #viimane_vol on tühi, võtad #vol veeru numbri 
-- seejärel võtad järgmise koodi ning tasks.md alt järgmise tsitaadi, mis lõppeb:
   --- numbriga + br või
   --- numbriga + reavahetus
    ---- kõik kuni numbrini läheb järgmise tagi sisse
<p class="quote" style="text-align: center;"></p>
    ------ kui on “,siis asenda "
    ------ kui on ” , siis asenda " 
    ------ kui on _sona_, siis asenda <em>sona</em>
    ------ kui on **sona**, siis asenda <strong>sona</strong>
    ------ "kui ,on" - siis "kui, on" ehk , ees ei ole tühikut ja taga on
    ------ kui on topelttühikud  ,siis eemalda üks neist
    ------ kui ...sona, siis ... sona
    ------ kui on .sona, siis on . sona - tühik vahele, sona algustäht jääb nii nagu on
    ---- number ise läheb selle tagi sisse
	<p style="text-align: center;"><span class="lk">lk </span></p>
    ----- kontrolli, et <p style="text-align: center;"><span class="lk">lk 123 </span></p> numbri ja spani ees ei oleks tühikut ehk peaks olema <p style="text-align: center;"><span class="lk">lk 123</span></p>
    ---- võta list.csv sama #pealkirja #caption veerust kood ja lisa iga tsitaadi bloki lõppu (pärast lk-numbrit)
   --- kui sama #pealkirja alla tuleb veel tsitaate siis, siis tee 4 reavahet
   --- kui sama # pealkirja alla ei tule rohkem tsitaate, siis tee 4 reavahet ja järgmine rida /**********/
   ---- lisa tasks.md-sse Tehtud alla #pealkirja ja tsitaatide arv. Uuemad tehtud lisa ettepoole.
   ---- kustuta Tegemata tööde alt tehtud tsitaadid.
   ----- kui list.csv #koik veerus puudub J
   ------ siis jäta Tegemata tööde, alla alles #pealkiri ja /*******/
   ------ kui #pealkiri ja /*****/ puudub, siis loo see
   ----- kui list.csv #koik veerus on J, siis eemalda ka Tegemata tööde alt #pealkiri ja /*************************/
   ---- Uuenda list.csv
   ----- viimane_vol quotes.md all, mis on viimane #pealkiri vol #nr
   ----- yles_vol mitu tsitaati on quotes.md-s selle #pealkirja all juba (tehtud tsitaatide arv)

   ```

   #Inimesele
   - J lisad list.cvs käsitsi
   - kui oled quotes.md all eemaldanud, siis anna käsk 
   vaata üle 
----võrdle list.csv ja quotes.md #pealkiri veergu ning uuenda list.csv faili #yles_vol numbrit
----- kui quotes.md all puudub #pealkiri ja list.csv #yles_vol veerus on 0 ja #koik veerus on J, siis küsi, kas soovin antud rida eemaldada
------ kui ütlen jah, siis eemalda rida ja ka tasks.md Tehtud alt vastav #pealkirja rida
