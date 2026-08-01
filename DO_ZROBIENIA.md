# DO ZROBIENIA — Parkova Hotel Strona
**Data:** 14.03.2026 | Aktualizacja @coo po sesji implementacyjnej

---

## 🔴 KRYTYCZNE (przed publikacją)

### 1. Google Analytics 4 — zastąp ID
**Plik:** `index.html` → linia ~19
```
Znajdź:   G-XXXXXXXXXX
Zastąp:   Twoim prawdziwym ID (np. G-ABC123XYZ)
```
**Jak zdobyć:** analytics.google.com → Utwórz konto → Strumień danych → skopiuj Measurement ID

---

### 2. Facebook Pixel — zastąp ID
**Plik:** `index.html` → linia ~29
```
Znajdź:   XXXXXXXXXXXXX
Zastąp:   Twoim prawdziwym ID piksela (16 cyfr)
```
**Jak zdobyć:** business.facebook.com → Events Manager → Pixel → Ustawienia → skopiuj Pixel ID

---

### 3. Formspree — skonfiguruj formularze (2 miejsca!)
**Plik:** `index.html` → wyszukaj: `FORMSPREE_ID` (występuje 2x — formularz kontaktowy + formularz callback przy kalkulatorze)
```
Znajdź:   https://formspree.io/f/FORMSPREE_ID
Zastąp:   https://formspree.io/f/TwójKod (np. xpwdrgkj)
```
**Jak zdobyć:**
1. Wejdź na formspree.io
2. Zarejestruj się za darmo
3. Utwórz nowy formularz → wpisz email docelowy
4. Skopiuj Form ID (8 znaków po /f/)
5. Darmowy plan: 50 zgłoszeń/miesiąc

---

### 4. ✅ Polityka Prywatności — ZROBIONE
Plik `polityka-prywatnosci.html` utworzony. RODO-compliant, 9 paragrafów, styl Parkova.

---

### 5. ✅ Regulamin — ZROBIONE
Plik `regulamin.html` utworzony. 10 paragrafów, spis treści, anulowanie, check-in/out, zwierzęta.

---

## 🟡 WAŻNE (w ciągu tygodnia po publikacji)

### 6. Konwertuj obrazy na WebP
Obecny format: PNG (wolniejsze ładowanie)
Zalecany format: WebP (30-80% mniejszy rozmiar)

**Narzędzia (darmowe):**
- squoosh.app — przeciągnij PNG, eksportuj jako WebP, jakość 80%
- cloudconvert.com — konwersja batch

**Pliki do konwersji:**
```
img/01_slider_glowne.png → 01_slider_glowne.webp
img/02_obiekt.png        → 02_obiekt.webp
img/03_galeria.png       → 03_galeria.webp
img/04_pokoj.png         → 04_pokoj.webp
img/05_zdj2.png          → 05_zdj2.webp
img/06_zdj4.png          → 06_zdj4.webp
img/07_zdj5.png          → 07_zdj5.webp
```

Po konwersji zaktualizuj nazwy plików w index.html (`.png` → `.webp`).

---

### 7. ✅ sitemap.xml — ZROBIONE
Plik `sitemap.xml` utworzony. Zawiera: stronę główną, politykę prywatności, regulamin.

---

### 8. ✅ robots.txt — ZROBIONE
Plik `robots.txt` utworzony. Allow: /, Disallow: /backup/

---

### 9. Zgłoś stronę do Google Search Console
1. Wejdź na search.google.com/search-console
2. Dodaj właściwość: rezydencjaparkowa.com
3. Zweryfikuj przez Google Analytics (jeśli GA4 już działa) lub plik HTML
4. Prześlij sitemap.xml

---

## ⚪ DO ROZWAŻENIA (opcjonalne)

### 10. Opublikuj prawdziwe opinie
Strona ma 6 przykładowych opinii. Zastąp prawdziwymi lub dodaj widżet Booking.com / Google Reviews.

### 11. Social media — zweryfikuj i aktywuj linki
W stopce dodano ikony FB/Instagram/WhatsApp z placeholder-owymi URL-ami.
```
Sprawdź i zastąp:
- facebook.com/rezydencjaparkova  → prawdziwy profil FB
- instagram.com/rezydencjaparkova → prawdziwy profil IG
- wa.me/48886120501               → już aktywny (numer recepcji)
```

### 12. ✅ Favicon — ZROBIONE
Plik `favicon.svg` utworzony (złote "P" na ciemnozielonym tle). Już podłączony w `<head>`.

### 13. Test formularzy po podłączeniu Formspree
Wyślij testowe zapytanie z obu formularzy i sprawdź czy email dochodzi na biuro@rezydencjaparkowa.com:
- [ ] Formularz kontaktowy (sekcja kontakt)
- [ ] Formularz callback przy kalkulatorze grupowym

### 14. Test na telefonie
Sprawdź:
- [ ] WhatsApp sticky CTA widoczny i klikalny (zastąpił starego FAB-a)
- [ ] Sticky CTA na dole działa
- [ ] Formularz kontaktowy działa
- [ ] Formularz callback przy kalkulatorze działa
- [ ] Kalkulator grupowy działa
- [ ] Hamburger menu otwiera się i zamyka
- [ ] Mapa ładuje się poprawnie

---

## ✅ ZROBIONE W TEJ SESJI

| # | Co | Kiedy |
|---|-----|-------|
| ✅ | SEO: FAQPage JSON-LD (7 pytań) | 14.03.2026 |
| ✅ | SEO: og:image absolutny URL, og:url, og:locale, og:site_name | 14.03.2026 |
| ✅ | SEO: Twitter Cards (summary_large_image) | 14.03.2026 |
| ✅ | SEO: canonical tag | 14.03.2026 |
| ✅ | Bug fix: toastIcon null reference (brak id na elemencie) | 14.03.2026 |
| ✅ | Bug fix: textContent → innerHTML (SVG w przycisku formularza) | 14.03.2026 |
| ✅ | Usunięto dead CSS: .phone-fab, fabPulse, fabWiggle | 14.03.2026 |
| ✅ | WhatsApp sticky CTA (zastąpił FAB) | 14.03.2026 |
| ✅ | Formularz callback przy kalkulatorze grupowym | 14.03.2026 |
| ✅ | Tracking: exit popup (GA4 exit_popup_shown + exit_popup_click, fbq ViewContent) | 14.03.2026 |
| ✅ | Tracking: callback_request (GA4 + fbq Lead) | 14.03.2026 |
| ✅ | Social media ikony w stopce (FB/IG/WhatsApp) | 14.03.2026 |
| ✅ | favicon.svg (złote "P" na zielonym) | 14.03.2026 |
| ✅ | robots.txt | 14.03.2026 |
| ✅ | sitemap.xml | 14.03.2026 |
| ✅ | polityka-prywatnosci.html (RODO, 9 §) | 14.03.2026 |
| ✅ | regulamin.html (10 §, spis treści) | 14.03.2026 |
| ✅ | 404.html (styl Parkova, telefon recepcji) | 14.03.2026 |
| ✅ | Git init + push do GitHub Pages | 14.03.2026 |

---

## KOLEJNOŚĆ NASTĘPNYCH DZIAŁAŃ

```
1. Formspree (5 min) → wstaw FORMSPREE_ID w 2 miejscach → formularz zacznie zbierać leady
2. Google Analytics (10 min) → wstaw G-XXXXXXXXXX → dane od pierwszej wizyty
3. Facebook Pixel (10 min) → wstaw XXXXXXXXXXXXX → możliwość reklam
4. Social media (5 min) → zweryfikuj URL-e FB/IG w stopce
5. Google Search Console (15 min) → zgłoś sitemap.xml → indeksowanie
6. Konwersja obrazów WebP (1h) → szybkość strony
7. Prawdziwe opinie gości → wiarygodność
```

---

**Kontakt do dewelopera:** biuro@rezydencjaparkowa.com
