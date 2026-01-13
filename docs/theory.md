# Teorijski dio – Segmentacija mreže

## 1. Uvod

Segmentacija mreže je postupak u kojem se jedna veća mreža dijeli na manje
dijelove kako bi se bolje kontrolirao pristup te smanjili sigurnosni rizici.
U praksi to znači da je mreža postavljena tako da svaki korisnik ili sustav
može pristupati samo onome što mu stvarno treba, a sve ostalo mu je
automatski blokirano. Na taj način napadač, čak i ako uspije upasti u jedan
dio mreže, ne može lako prijeći na druge sustave.

U ovom projektu obrađujemo osnovne pojmove segmentacije, njezinu ulogu u
sigurnosti informacijskih sustava te razloge zbog kojih je postala važan dio
obrane od modernih prijetnji, poput ransomware napada. Cilj je objasniti što
segmentacija radi, zašto je korisna i kako se primjenjuje u stvarnim
okruženjima, bez previše tehničkog kompliciranja.

---

## 2. Definicija segmentacije

Segmentacija mreže predstavlja način organizacije mreže tako da se jedna
veća cjelina podijeli na više manjih, logički odvojenih segmenata. Svaki
segment djeluje kao zasebno okruženje s jasno definiranim pravilima pristupa,
što omogućuje bolju kontrolu nad time tko može komunicirati s kojim
sustavima [6]. Time se smanjuje mogućnost da neovlašteni korisnici ili
potencijalni napadači dođu do osjetljivih podataka ili kritičnih resursa.

Kada se primjenjuje u stvarnoj mreži, segmentacija omogućuje jasnu podjelu
korisnika i sustava. Najčešće se postiže korištenjem VLAN-ova, različitih
mrežnih zona na firewallu ili jednostavnim odvajanjem subnetova. Primjerice,
računala iz financijskog odjela ne bi trebala komunicirati s računalima iz
odjela prodaje, osim ako za to postoji jasan razlog. Isto tako, poslužitelji
koji sadrže osjetljive podatke mogu biti smješteni u posebno izoliranom dijelu
mreže, kojem može pristupiti samo ograničen broj korisnika.

Cilj segmentacije nije samo „razdvojiti” mrežu, nego i jasno definirati
pravila pristupa, smanjiti mogućnost širenja napada, povećati preglednost
prometa i olakšati primjenu sigurnosnih politika. Takva podjela mreže
postala je vrlo važna u modernim organizacijama jer napadači danas najčešće
ne napadaju odmah najosjetljivije sustave, nego se pokušavaju postupno
kretati kroz mrežu dok ne dođu do vrijednih podataka. Segmentacija taj put
drastično otežava.

---

## 3. Primjena segmentacije u zaštiti informacijskih sustava

Segmentacija mreže omogućuje da se unutar organizacije jasno odrede granice
između različitih dijelova sustava te da se kontrolira pristup resursima
prema stvarnim potrebama korisnika i aplikacija. Kada je mreža postavljena
kao jedna velika cjelina, kompromitiranje jednog uređaja često napadaču
otvara put prema ostalim sustavima. Podjela mreže na manje logičke cjeline
značajno otežava takvo kretanje i smanjuje potencijalnu štetu.

Odvajanje osjetljivih sustava, poput financijskih servisa ili baza podataka,
u zasebne segmente omogućuje primjenu preciznih pravila pristupa. Takav
pristup smanjuje mogućnost neovlaštenog ulaza, ali i rizik ljudske pogreške,
jer se korisnicima dodjeljuje samo onaj pristup koji im je nužan za rad.

Segmentacija ima važnu ulogu i u zaštiti od modernih prijetnji, osobito
ransomware napada, čiji je cilj brzo širenje kroz mrežu. Ako se takav napad
dogodi unutar segmentirane mreže, širenje se može zaustaviti u okviru jednog
segmenta, čime se štiti ostatak sustava. Na sličan način segmentacija
nadopunjuje principe Zero Trust modela, u kojem se pristup ne dodjeljuje
unaprijed, nego isključivo prema stvarnoj potrebi.

Zbog svega navedenog segmentacija je važan dio sigurnosne strategije
organizacija, jer povećava preglednost nad mrežom, smanjuje rizike i pruža
dodatnu razinu zaštite osjetljivim dijelovima informacijskog sustava.

---

## 4. Važnost segmentacije u modernim mrežama

U današnjim organizacijama mrežni sustavi postaju sve složeniji, a svaki od
njih može predstavljati potencijalnu točku ulaza za napadače. Upravo zbog
takvog okruženja sigurnosne mjere moraju biti postavljene tako da se prijetnje
mogu zaustaviti što ranije i što bliže izvoru. Jedan od pristupa koji to
omogućuje jest koncept podjele mreže na manje cjeline s jasno definiranim
pravilima komunikacije, što se pokazalo iznimno učinkovitim kod obrane od
suvremenih napada.

Posebno je to vidljivo kod modela Zero Trust, koji se temelji na pretpostavci
da se pristup ne dodjeljuje automatski ni jednom korisniku ili uređaju, bez
obzira na to gdje se nalaze u mreži [1]. U takvom modelu svaki zahtjev za
pristup prolazi provjeru, a komunikacija se dopušta samo kada je nužna.
Podržavanje ovakvog pristupa znatno je jednostavnije u okruženju gdje su
sustavi međusobno odvojeni i gdje je moguće precizno definirati granice
između različitih funkcionalnih cjelina [2].

Danas se sigurnosne arhitekture sve češće temelje na jasnoj kontroli prometa,
precizno definiranim pravilima pristupa i odvojenosti osjetljivih sustava. Na
taj način povećava se razina zaštite i smanjuje mogućnost da jedan
sigurnosni propust ugrozi veći dio mreže. Upravo zbog toga ovakav pristup sve
više postaje uobičajena praksa u modernim mrežnim okruženjima [7].
