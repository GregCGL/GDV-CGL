# Luxa Moments — onafhankelijke statische website

Laatste technische controle: 18 juni 2026.

## Doel

Deze repository bevat een zelfstandige statische versie van `www.luxamoments.be` voor hosting in eigen beheer. De visuele vormgeving, teksten, beelden, navigatie en boekingsflow blijven zo dicht mogelijk bij de bestaande website.

## Pagina's

- `/`
- `/over-ons`
- `/product/vlinders`
- `/algemene-voorwaarden`
- `/terms`

## Integraties

### Booqable

De bestaande boekingsflow blijft extern lopen via:

- `https://luxa-events.booqableshop.com/`

Producten, beschikbaarheid, checkout en betaalflow worden dus verder beheerd in Booqable.

### Mollie

Er staat geen directe Mollie-code in deze statische website. Betalingen lijken via de Booqable-checkout te verlopen. Controleer daarom bij livegang:

1. Mollie-configuratie in Booqable.
2. Testbetaling via Booqable.
3. Livebetaling via Booqable.
4. Eventuele webhooks/statussen in Booqable en Mollie.

## Technische structuur

- HTML-pagina's staan in de root en submappen.
- CSS en beelden staan in `/assets`.
- `_redirects` is voorzien voor hosts die Netlify-achtige redirects ondersteunen.
- `vercel.json` is aanwezig indien later Vercel gebruikt wordt.

## Lokaal openen

Open `index.html` rechtstreeks in een browser.

## Onderhoud

- Teksten aanpassen in de HTML-bestanden.
- Beelden vervangen in `/assets`.
- Booqable-producten en betalingen aanpassen in Booqable/Mollie, niet in deze statische bestanden.
