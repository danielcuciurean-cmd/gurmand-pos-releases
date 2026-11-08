# Gurmand TV – afișaj meniu pe televizoare

Pagina `index.html` rotește automat pozele de pe fiecare televizor, cu tranziție fade.
Fiecare televizor are propriul link:

| Televizor | Link |
|-----------|------|
| TV 1 | `https://danielcuciurean-cmd.github.io/gurmand-pos-releases/tv/?tv=1` |
| TV 2 | `https://danielcuciurean-cmd.github.io/gurmand-pos-releases/tv/?tv=2` |
| TV 3 | `https://danielcuciurean-cmd.github.io/gurmand-pos-releases/tv/?tv=3` |

(Linkurile merg după ce activezi GitHub Pages, vezi mai jos.)

## Pornire (o singură dată)
1. GitHub → repo `gurmand-pos-releases` → **Settings → Pages** → Source: *Deploy from a branch*, Branch: `main`, folder `/ (root)` → Save.
2. După 1-2 minute linkurile de mai sus funcționează.
3. Pe fiecare televizor: deschizi browserul, intri pe linkul lui, îl salvezi la favorite/pagină de start, apoi ecran complet.

## Cum schimbi pozele (de oriunde)
1. Exporți slide-urile din Canva ca **PNG, 1366×768** (Share → Download → PNG).
2. GitHub → folderul `tv/tv1` (sau `tv2`, `tv3`) → **Add file → Upload files** → tragi pozele → Commit.
3. Editezi `slides.json` din același folder (creion) ca să pui numele fișierelor în ordinea dorită.
4. În 1-2 minute (publicare GitHub) + maximum 2 minute (televizorul verifică singur) se schimbă pe ecran. Nu trebuie să ai nimic la televizor.

## slides.json
```json
{
  "seconds": 10,
  "slides": ["1.png", "2.png", {"file": "pizza.png", "seconds": 15}]
}
```
- `seconds` = cât stă fiecare poză (implicit 10).
- Un slide poate avea timp propriu (obiectul cu `file` + `seconds`).
- Merg și video-uri `.mp4` / `.webm` (fără sunet).

## Reguli utile
- Folosește aceeași dimensiune 16:9 pentru toate pozele. Dacă pozele sunt altfel, apar benzi negre.
- Nume de fișier fără spații sau diacritice (ex: `pizza.png`, nu `Pizză 1.png`).
- Dacă pică internetul, televizorul continuă cu ce rula deja.
- Pagina se reîncarcă singură la fiecare 6 ore.
- Pozele din folderele `tv1`, `tv2`, `tv3` acum sunt doar de test: înlocuiește-le.
