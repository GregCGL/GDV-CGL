# One.com deployment-instructies voor Luxa Moments

## Wat uploaden?

Upload de **inhoud** van deze map naar de webroot van One.com:

- `index.html`
- `_redirects`
- `vercel.json` mag blijven staan maar is niet noodzakelijk voor One.com
- `README.md` en `ONECOM_DEPLOYMENT.md` hoeven niet publiek, maar mogen technisch gezien geen kwaad
- mappen:
  - `assets/`
  - `product/`
  - `algemene-voorwaarden/`
  - `terms/`

Belangrijk: upload niet de bovenliggende map als extra mapniveau. De homepage moet direct bereikbaar zijn als:

- `https://www.luxamoments.be/index.html`
- en normaal ook als `https://www.luxamoments.be/`

## Waar uploaden bij One.com?

Bij klassieke One.com-webhosting is de webroot meestal één van deze locaties:

- `public_html`
- `httpdocs`
- of de hoofdmap die One.com File Manager als websiteroot toont

Plaats de bestanden in de map waar de huidige publieke `index.html` verwacht wordt.

## ZIP uploaden of folderinhoud?

- Als One.com File Manager ZIP-extractie ondersteunt: upload `luxa-moments-independent-site.zip`, pak uit en verplaats de **inhoud** van de uitgepakte map naar de webroot.
- Als ZIP-extractie niet beschikbaar is: upload de folderinhoud rechtstreeks via FTP/SFTP of File Manager.

## Na upload testen

1. Open `https://www.luxamoments.be/`.
2. Test desktop en mobiel.
3. Test navigatie naar:
   - `/product/vlinders/`
   - `/algemene-voorwaarden/`
   - `/terms/`
4. Controleer of alle beelden laden.
5. Klik alle boekingsknoppen en controleer dat ze naar `https://luxa-events.booqableshop.com/` gaan.
6. Test de Booqable-reservatieflow.
7. Test een Mollie-testbetaling via Booqable.
8. Controleer telefoon- en e-maillinks.
9. Controleer SSL-slotje in de browser.

## DNS

Als de domeinnaam al bij One.com staat en dezelfde hosting gebruikt wordt, is meestal geen DNS-wijziging nodig. Als de site naar een nieuwe One.com-hostingomgeving verhuist, volg dan de DNS-instructies van One.com voor `luxamoments.be` en `www.luxamoments.be`.
