# OK-Trainer — nasazení na GitHub Pages

Ve složce jsou 3 soubory, které spolu patří a musí zůstat ve stejném adresáři:
- `index.html` — samotná aplikace
- `manifest.json` — popisuje appku pro instalaci na plochu
- `icon.svg` — ikonka

## Varianta A — přes webové rozhraní GitHubu (bez příkazové řádky)

1. Přihlas se na [github.com](https://github.com) a klikni na **New repository**.
2. Zadej název, např. `harec-trainer`, nastav ho jako **Public** (u GitHub Pages zdarma musí být veřejné), a repozitář vytvoř (nezaškrtávej žádné "initialize with README" apod. — je to jedno, jen to pak trochu jinak nahraješ).
3. Na stránce nového repozitáře klikni na **Add file → Upload files**.
4. Přetáhni tam všechny 3 soubory (`index.html`, `manifest.json`, `icon.svg`) najednou.
5. Dole potvrď **Commit changes**.
6. Jdi do **Settings** repozitáře (nahoře v menu repozitáře) → v levém menu **Pages**.
7. U „Build and deployment" → „Source" vyber **Deploy from a branch**.
8. U „Branch" vyber `main` a složku `/ (root)`, klikni **Save**.
9. Počkej minutu, obnov stránku — nahoře se objeví zelený pruh s adresou typu:
   `https://<tvoje-uživatelské-jméno>.github.io/harec-trainer/`
10. Tuhle adresu otevři v Chromu na mobilu → ⋮ menu → **Nainstalovat a vytvořit zástupce** (dřív „Přidat na plochu"). Tentokrát by se možnost měla nabídnout, protože stránka běží přes `https://`.

## Varianta B — přes git (pro tebe asi rychlejší)

```bash
cd harec-trainer
git init
git add index.html manifest.json icon.svg
git commit -m "OK-Trainer flashcards"
git branch -M main
git remote add origin https://github.com/<tvoje-uživatelské-jméno>/harec-trainer.git
git push -u origin main
```

Pak stejně jako v bodě 6–9 výše: **Settings → Pages → Deploy from a branch → main / (root) → Save**.

## Pozn. k aktualizacím

Pokud budeš chtít někdy přidat další kartičky nebo upravit obsah, stačí nahradit `index.html` novou verzí (přes "Upload files" znovu, nebo `git push`) — adresa i nainstalovaná ikonka na ploše zůstanou stejné, obsah se jen aktualizuje.
