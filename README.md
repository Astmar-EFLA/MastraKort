# Mastrakort

Einfaldur vefskoðari fyrir möstur (afleggjari af Jarðkönnun-appinu, án SharePoint; útlit samkvæmt Efla-vörumerkjahandbók). Opinn úr síma eða tölvu, engin uppsetning.

**Hvað hann gerir**
- Les hnitaskrá (CSV) með mastranöfnum og sýnir möstrin á korti (OSM / loftmynd) og í leitarhæfum lista.
- Smelltu á mastur til að zooma að því. **🚗 Leið** opnar leiðsögn beint á mastrið í Google Maps; í sprettglugganum er líka „Sýna í Google Maps“ og „Afrita hnit“.
- **Lokið:** merktu mastur lokið með „Merkja lokið“ í sprettglugganum eða hakreitnum í listanum. Framvinda sést efst í listanum, hægt er að sía óloknar/loknar og sækja stöðuna sem CSV (⤓ Mín gögn). Staðan vistast í tækinu.
- Mastursnúmerið (tölustafir fremst í nafni, t.d. 12 í „12-FAJ“) sést í hring á korti og í listanum.
- ◎ zoomar á staðsetningu símans, ⛶ fullur skjár.
- ⌖ tekur punkt á staðsetningu þinni (heiti + athugasemd), ⏺ tekur upp GPS-slóð. Allt vistast í tækinu (virkar án nets) og fæst sótt sem GPX eða GeoJSON í ⤓ „Mín gögn“.

**Hnitaskráin**
- `masts.csv` í sömu möppu er sótt sjálfkrafa við opnun (uppfærðu hana á GitHub og allir sjá nýju möstrin).
- Eða veldu CSV-skrá / vefslóð í ⚙ stillingum (vistast í tækinu). Hægt er að nota `?csv=<slóð>` í vefslóðinni til að benda á aðra skrá, t.d. `…/index.html?csv=https://raw.githubusercontent.com/<notandi>/<repo>/main/masts.csv`.
- Haus er nauðsynlegur. Nafn: dálkur sem heitir `Nafn`, `Heiti`, `Name`, `Nr.` … (annars fyrsti dálkur). Hnit: `X`/`Y` (eða `Austur`/`Norður`) eða `Lat`/`Lon`.
- Hnitakerfi greinist sjálfkrafa: ISN93 (X≈300–700 þús.), ISN2016 (X > 2 milljónir) eða WGS84. Hægt að þvinga í stillingum.
- **GeoJSON** er líka stutt sem mastraskrá (`masts.geojson` er reynd ef `masts.csv` vantar, eða veldu skrána í stillingum): Point-hlutir með nafn í `properties.nafn` / `heiti` / `name`. `properties.lokid = true` (og valfrjálst `lokid_timi`) merkir mastur lokið við innlestur. „Möstur með stöðu (GeoJSON)“ í ⤓ Mín gögn flytur mastrana út með `lokid` svo hægt sé að setja skrána aftur á GitHub.
- Skilatákn: `;`, `,` eða tab. Aðrir dálkar birtast í sprettglugga mastursins.

Sýnishorn: sjá `masts.csv`.

**Birting á GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root.
