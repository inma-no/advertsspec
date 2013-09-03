## Fysisk størrelse:
* Høyde: 225px
* Bredde: 100%
* Størrelse (kb):
** Maks 100 kb i arkivert tilstand (alle filer komprimert/zippet sammen).
** Du kan benytte jQuery-biblioteket uten å medregne det i størrelsen på reklamen. Men dette krever at du benytter siste versjon av jQuery.min.js fra [Googles CDN-tjeneste](https://developers.google.com/speed/libraries/devguide#jquery) (f.eks [jQuery 2.0.0](//ajax.googleapis.com/ajax/libs/jquery/2.0.0/jquery.min.js))

## Begrensninger:
* Viewport kan ikke settes til device width i reklamen 

		<meta name="viewport" content="width=devicewidth">

* Bruk av innebygd geo-lokasjon er ikke tillatt
* HTML-filen skal kun bestå av én fil som inkluderer all css
* Maksimum 2 requests til JavaScript-bibliotek (en lokal og en ekstern).
* Animasjon i reklamen før bruker har interagert med den, må være av typen CSS3 (dvs GPU-basert). JavaScript-animasjon (eks jQuery) er ikke tillatt før bruker berører reklamen (for eksempel på sveip). For tutorial og eksempler på CSS3-animasjoner, se http://tinyurl.com/lg6yx6e

## Klikkteller:
Legges inn av annonseutvikler og følgende metode må brukes:

	<div id="Banner" onclick="window.open('http://www.url.no','new_window');" style="display:block;">

## Tredjepartskode:
* Sendes over som Javascript-kode

## Bruk av gamle formater:
Mange merkevareannonser består av et enkelt bilde som er tilpasset i høyde og bredde til forskjellige formater (f.eks. én grafikk tilpasset iPhone og én til iPad).

Fra og med 26. august skal bilderbannere (PNG/JPEG/GIF) produseres slik at det fyller hele
bredden og høyden i portrett, mens det midtstilles i landskap uten skalering. Formatstørrelsen er
laget med utgangspunkt i iPhone og iPad.
* Mobil: 310*225 maks 50 KB
* Tablet: 758*225 maks 100 KB