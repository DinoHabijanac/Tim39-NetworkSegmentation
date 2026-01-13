# Metodologija rada i opis laboratorijskog okruženja

Kako bismo teorijske koncepte segmentacije mreže povezali s praktičnom
primjenom, u okviru ovog projekta koristili smo laboratorijski pristup.
Umjesto rada na stvarnoj produkcijskoj mreži, segmentaciju smo implementirali
u kontroliranom virtualnom okruženju, što nam je omogućilo sigurno testiranje
različitih konfiguracija i scenarija bez rizika za stvarne sustave.

Za izradu laboratorijskog okruženja odabrali smo alat Cisco Packet Tracer,
koji se često koristi u obrazovne svrhe zbog mogućnosti simulacije mrežnih
uređaja i konfiguracije VLAN-ova, rutiranja i sigurnosnih pravila. Iako alat
ne može u potpunosti zamijeniti rad u stvarnom mrežnom okruženju, omogućio
nam je jasno razumijevanje osnovnih principa segmentacije i kontrole prometa,
što je bilo u skladu s ciljevima projekta.

Metodologiju rada temeljili smo na postupnom razvoju mrežne konfiguracije.
Najprije smo izradili osnovnu topologiju bez sigurnosnih ograničenja kako
bismo provjerili osnovnu povezivost između mrežnih segmenata. Nakon toga smo
uveli pravila kontrole pristupa, čime smo mogli usporediti ponašanje mreže
prije i nakon primjene sigurnosnih mehanizama. Takav pristup omogućio nam je
jasnije razumijevanje razlike između same VLAN segmentacije i stvarne
kontrole prometa.

Poseban naglasak stavili smo na razdvajanje korisničkog, serverskog i
administratorskog dijela mreže. Ovakvu podjelu odabrali smo jer se često
koristi u praksi, a preporučena je i u relevantnim sigurnosnim smjernicama.
Uz osnovnu segmentaciju, u metodologiju smo uključili i primjenu ACL pravila
te mikrosegmentacije na razini pojedinih sustava, čime smo demonstrirali
višeslojni sigurnosni pristup.
