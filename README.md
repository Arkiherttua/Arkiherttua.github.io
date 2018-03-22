# Arkiherttua.github.io

Testailua varten luotu nettisivu.




# Nettisivut Githubiin

Tällä ohjeella saat luotua omat nettisivut Github-sivuston palvelimelle. Ne löytyvät osoitteesta omakäyttäjätunnus.github.io :)

## Nettisivu-repositorion luonti

1. Mene Githubin sivulle github.com

2. Luo käyttäjätunnus Githubiin (tunnuksesta tulee osa sivun osoitetta!). Vahvista sen jälkeen rekisteröityminen käymällä sähköpostissa klikkaamassa linkkiä

3. Kirjaudu sisään. Päädyt omalle profiilisivullesi, jossa näkyvät kaikki projektisi (Github-sivusto on tarkoitettu erinäisten koodiprojektien säilytyspaikaksi)

4. Oikealta löytyy vihreä &quot;new repository&quot;-nappi, josta saat luotua uuden repositorion (&quot;säilytyspaikan&quot;, kansion koodausprojektillesi)

5. Nimeä repositorio täsmälleen käyttäjänimesi mukaiseksi (niin Github tietää luoda repositoriota vastaavan sivuston).

Voit myös antaa sille Githubissa näkyvän kuvauksen (description). Näkyvyyden on oltava julkinen (public), sillä yksityisistä repositorioista pitää maksaa. Kaikki internetissä voivat siis katsoa koodiasi, nettisivun lisäksi. Ruksaa &quot;Initialize this repository with a README&quot;, jotta saat repositoriolle esittelytiedoston (readme). Viimeisiin kahteen nappiin gitignoresta tai lisenssistä ei tarvitse koskea.

6. Luotuasi repositorion, sinulle pitäisi aueta repositorion sivu, josta pääset muokkaamaan sivuasi.

## Sivuston luominen ja päivittäminen

Repositoriosi sivulla on paljon kaikenlaista, mutta olennaisimpia ovat:

- yläoikealta voit kirjautua ulos ja muuttaa asetuksiasi

- Create new file -napista luodaan uusi tiedosto

- Listassa näet kaikki luomasi sivut, klikkaamalla pääset katsomaan ja muokkaamaan niiden koodia

- Alimpana näkyy README.md -tiedoston sisältö eli repositoriosi kuvaus.

1. Luodaan index eli etusivu: luo uusi tiedosto, ja nimeä se index.html. Kirjoita sinne html-sivun minimirunko:

```html
<!DOCTYPE html>
&lt;html&gt;
 &lt;title&gt;
  Tähän sivun otsikko (yläpalkissa näkyvä)
 &lt;/title&gt;
 &lt;body&gt;
  Tänne sivun sisältö, teksti, kuvat, linkit jne.
 &lt;/body&gt;
&lt;/html&gt;
```

Tallenna tiedosto painamalla nappia &quot;commit changes&quot; eli &#39;tee muutokset&#39; alareunassa. Voit kirjoittaa päivitysviestin, jos haluat, mutta se ei ole pakollista näin yksinkertaisessa projektissa.

2. Avaa nyt luomasi sivu menemällä osoitteeseen käyttäjätunnuksesi.github.io ja katso miltä näyttää HUOM: joskus kestää pari minuuttia, että muutokset päivittyvät näkyviin

3. Sivua voi muokata klikkaamalla repositorion listasta ensin sen koodin näkyviin ja sitten koodilaatikon yläoikealla pientä kynän kuvaa klikkaamalla.

## Navigaatiopalkin toteutus

Tehdään navigaatiopalkki, joka on helppo laittaa näkymään joka sivulla. Tehdään se erillikseksi tiedostoksi, joka jQuery JavaScript-kirjaston avulla laitetaan näkymään kaikilla sivuilla.

1. Luo navigaatio.html niminen tiedosto

2. Tee sinne lista linkkejä: yksinkertaisimmillaan peräkkäin vaan
 &lt;a href="http://sivunosoite.com"> Linkin teksti</a><br>

3. Mene index.html tai muuhun tiedostoon jonne haluat navigaatiopalkin. Sinne pitää laittaa

- linkki jQuery-kirjastoon: &lt;script src=&quot;https://code.jquery.com/jquery-1.10.2.js" </script>;

- Koodinpätkä, jolla saadaan navigaatio näkymään:

&lt;div id=&quot;navigaationsijainti&quot;&gt;&lt;/div&gt; &lt;!-- Tämän rivin sijainti määrää paikan, johon navigaatio ilmestyy--&gt;

&lt;!-- script-tagin sisällä on varsinainen koodi, joka lataa navigaatio.html tiedoston sisällön tähän tiedostoon--&gt;

&lt;script&gt;

 $(function(){

 $(&quot;#navigaationsijainti&quot;).load(&quot;navigaatio.html&quot;);

 });

&lt;/script&gt;

# HTML-cheatsheet

Eli tärkeimmät komennot

**&lt;html&gt;&lt;/html&gt;** tähän väliin tulee KAIKKI html-tiedoston sisältö, sitä edeltää vain &lt;!Doctype html&gt;-tagi

**&lt;title&gt;&lt;/title&gt;** Sivun selaimen yläpalkissa näkyvä otsikko

**&lt;head&gt;&lt;/head&gt;**

**&lt;body&gt;&lt;/body&gt;** Tänne sivun näkyvä sisältö

**&lt;div&gt;&lt;/div&gt;** eli division eli osuus: tietty yhteen kuuluva osa sivua, esim. otsikko ja sitä seuraava tekstikappale

**&lt;h1&gt;&lt;/h1&gt;** Pääotsikko (myös h2, h3, h4, h5 olemassa, isompi numero on aina pienempi otsikko)

**&lt;p&gt;&lt;/p&gt;** eli paragraph eli (teksti)kappale

**&lt;br&gt;** rivinvaihto

**&lt;a href=&quot;http://sivunosoite.com"> Linkin teksti&lt;/a&gt;** Linkki 

**&lt;img src=&quot;kuvannimi.gif&quot; alt=&quot;teksti, jos kuvaa ei näykään&quot;&gt;** Kuva

**&lt;!-- kommentti, täällä sisällä oleva teksti ei näy itse sivulla--&gt;** (paitsi jos katsoo sivun koodia, älä siis kirjoita salaisuuksia!)

**Jotta saat jQueryllä toteutun navigaatiopalkin toimimaan, tarvitsen linkin jQuery-kirjastoon:**

&lt;script src=&quot; [https://code.jquery.com/jquery-1.10.2.js](https://code.jquery.com/jquery-1.10.2.js)&quot;&gt;&lt;/script&gt;

**Jos haluat tehdä sivun ulkonäön muotoilut Bootstrap-kirjastolla, tarvitset nämä linkit siihen:**

&lt;link rel=&quot;stylesheet&quot; href=&quot;https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css&quot; integrity=&quot;sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u&quot; crossorigin=&quot;anonymous&quot;&gt;
&lt;!-- Optional theme -->

&lt;link rel=&quot;stylesheet&quot; href=&quot;https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap-theme.min.css&quot; integrity=&quot;sha384-rHyoN1iRsVXV4nD0JutlnGaslCJuC7uwjduW9SVrLvRYooPp2bWYgmgJQIXwl/Sp&quot; crossorigin=&quot;anonymous&quot;&gt;
&lt;!-- Latest compiled and minified JavaScript -->

&lt;script src=&quot;https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js&quot; integrity=&quot;sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa&quot; crossorigin=&quot;anonymous&quot;&gt;&lt;/script&gt;


