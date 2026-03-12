# Dark UI — Cheat Sheet Visuelle

---

## 1. FONDS — Ne jamais utiliser le noir pur

```
#000000  ❌  trop cru
#0a0a0f  ✅  noir bleuté (froid, tech)
#0d0d0d  ✅  noir neutre (universel)
#0f0e17  ✅  noir chaud violacé (premium)
#0a0f0d  ✅  noir verdâtre (nature, finance)
```

---

## 2. PALETTES — Couleurs qui s'harmonisent

### Violet + Cyan (tech / dashboard)
```
Fond      → bg-[#0a0a0f]
Accent 1  → violet-500   #8b5cf6
Accent 2  → sky-400      #38bdf8
Texte     → white / white/60 / white/30
Bordure   → white/10
```

### Sunset (créatif / portfolio)
```
Fond      → bg-[#0f0a0a]
Accent 1  → orange-500   #f97316
Accent 2  → pink-500     #ec4899
Accent 3  → yellow-400   #fbbf24
Bordure   → white/10
```

### Emerald (finance / crypto)
```
Fond      → bg-[#080f0c]
Accent 1  → emerald-400  #34d399
Accent 2  → teal-500     #14b8a6
Texte     → white / white/60
Bordure   → emerald-900/50
```

### Golden (luxury / pricing)
```
Fond      → bg-[#0c0900]
Accent 1  → yellow-400   #fbbf24
Accent 2  → amber-500    #f59e0b
Accent 3  → orange-400   #fb923c
Bordure   → yellow-900/40
```

### Mono Violet (SaaS premium)
```
Fond      → bg-[#0d0b14]
Accent 1  → violet-400   #a78bfa
Accent 2  → purple-600   #9333ea
Accent 3  → fuchsia-500  #d946ef
Bordure   → violet-900/40
```

---

## 3. TYPOGRAPHIE — Règle des 4 niveaux

```
Titre         → text-white font-bold
Corps         → text-white/60
Secondaire    → text-white/40
Label section → text-white/30 text-[11px] uppercase tracking-widest
```

### Fonts qui marchent sur fond sombre

| Style      | Font                    | Import Google Fonts                       |
|------------|-------------------------|-------------------------------------------|
| Tech       | `Geist Mono`            | pas besoin si Next.js                     |
| Premium    | `Playfair Display`      | `family=Playfair+Display:wght@700;900`    |
| Moderne    | `DM Sans`               | `family=DM+Sans:wght@300;400;600`         |
| Editorial  | `Cormorant Garamond`    | `family=Cormorant+Garamond:wght@300;600`  |
| Futuriste  | `Syne`                  | `family=Syne:wght@400;700;800`            |
| Propre     | `Outfit`                | `family=Outfit:wght@300;400;600;700`      |

> Évite : Inter, Roboto, Arial — trop génériques.

---

## 4. CARDS — Les 3 recettes

### Recette 1 — Glass (fond blanc semi-transparent)
```html
<div class="
  bg-white/5
  backdrop-blur-md
  border border-white/10
  rounded-2xl p-5
">
```
→ Effet vitrine, moderne. Parfait sur fond avec blobs colorés.

### Recette 2 — Solid dark (fond sombre uni)
```html
<div class="
  bg-[#0d0d14]
  border border-white/10
  rounded-2xl p-5
">
```
→ Plus lisible, contenu-first. Idéal pour formulaires et listes.

### Recette 3 — Glow card (halo de lumière interne)
```html
<div class="relative overflow-hidden
  bg-[#0d0d14]
  border border-white/10
  rounded-2xl p-5
">
  <!-- Halo dans un coin -->
  <div class="absolute -top-10 -left-10
              w-32 h-32 rounded-full
              bg-violet-500 opacity-20 blur-[40px]
              pointer-events-none">
  </div>
  <div class="relative z-10">contenu</div>
</div>
```
→ C'est ça qui donne le "coin lumineux" sur une card.

---

## 5. BORDURES — Subtiles mais essentielles

```
border border-white/8    → presque invisible, très élégant
border border-white/10   → standard, le plus utilisé
border border-white/20   → hover state, ou card active
border border-violet-500/30  → bordure colorée subtile (accent)
border border-yellow-400/20  → bordure golden
```

### Hover interactif sur bordure
```html
<div class="border border-white/10 hover:border-white/25
            transition-all duration-300">
```

### Bordure avec glow coloré (effet premium)
```html
<div class="border border-violet-500/40
            shadow-[0_0_20px_rgba(139,92,246,0.15)]">
```

---

## 6. EFFETS LIGHT — Les blobs et halos

### Blob global (fond de page)
```html
<!-- Va dans le conteneur principal, en absolute -->
<div class="absolute w-[500px] h-[500px]
            -top-32 -left-32
            rounded-full
            bg-violet-600
            opacity-20
            blur-[100px]
            pointer-events-none">
</div>
```

### Halo de coin sur une card
```html
<!-- Dans une card avec overflow-hidden -->
<div class="absolute -top-8 -right-8
            w-24 h-24 rounded-full
            bg-sky-400 opacity-30 blur-[30px]
            pointer-events-none">
</div>
```

### Spotlight (lumière centrale)
```html
<div class="absolute top-0 left-1/2 -translate-x-1/2
            w-[300px] h-[1px]
            bg-gradient-to-r from-transparent via-violet-400 to-transparent
            opacity-60">
</div>
```
→ Ligne lumineuse en haut d'une card, très utilisée dans les UI premium.

### Recette 3 blobs pour une page complète
```html
<!-- Blob haut gauche -->
<div class="absolute -top-40 -left-40 w-[500px] h-[500px]
            rounded-full bg-violet-600 opacity-20 blur-[120px] pointer-events-none"></div>

<!-- Blob milieu droite -->
<div class="absolute top-1/2 -right-20 w-[400px] h-[400px]
            rounded-full bg-sky-500 opacity-15 blur-[90px] pointer-events-none"></div>

<!-- Blob bas centre -->
<div class="absolute -bottom-20 left-1/3 w-[350px] h-[350px]
            rounded-full bg-pink-500 opacity-15 blur-[80px] pointer-events-none"></div>
```

---

## 7. EFFET GLASSMORPHISME — Recette exacte

```html
<div class="
  bg-white/5              ← fond très transparent
  backdrop-blur-md        ← flou du fond (8px)
  border border-white/10  ← bordure lumineuse fine
  rounded-2xl
  shadow-xl shadow-black/30  ← ombre pour profondeur
">
```

### Niveaux de flou
```
backdrop-blur-sm   → 4px  (léger)
backdrop-blur-md   → 8px  (standard ✅)
backdrop-blur-lg   → 12px (fort)
backdrop-blur-xl   → 24px (très fort, attention aux perfs)
```

### Niveaux de transparence du fond
```
bg-white/3   → quasi invisible (très subtil)
bg-white/5   → standard glassmorphisme ✅
bg-white/8   → un peu plus visible
bg-white/10  → limite du glass, devient opaque
```

> La combinaison magique : `bg-white/5` + `backdrop-blur-md` + `border border-white/10`

---

## 8. EFFET GOLDEN — Luxury / Pricing

```html
<!-- Card golden -->
<div class="relative overflow-hidden
  bg-gradient-to-br from-yellow-900/30 via-[#0d0900] to-[#0d0900]
  border border-yellow-400/20
  rounded-2xl p-5
  shadow-[0_0_30px_rgba(251,191,36,0.08)]
">
  <!-- Halo doré coin haut droite -->
  <div class="absolute -top-10 -right-10 w-32 h-32
              rounded-full bg-yellow-400 opacity-15 blur-[40px]
              pointer-events-none"></div>

  <div class="relative z-10">
    <p class="text-yellow-400/60 text-[11px] uppercase tracking-widest">Premium</p>
    <p class="text-yellow-300 font-bold text-3xl mt-1">29€</p>
  </div>
</div>
```

### La palette golden exacte
```
Fond card      → from-yellow-900/30
Bordure        → border-yellow-400/20
Glow shadow    → shadow-yellow-400/10
Label          → text-yellow-400/60
Titre          → text-yellow-300
Valeur clé     → text-yellow-200 font-bold
Halo blob      → bg-yellow-400 opacity-15 blur
```

---

## 9. RÉCAP — Les règles d'or

```
✅ Fond         → jamais noir pur, toujours teinté
✅ Blobs        → opacity entre 15-25, blur entre 80-120px
✅ Bordures     → white/10 au repos, white/20 au hover
✅ Glass        → bg-white/5 + backdrop-blur-md + border white/10
✅ Halo card    → petit blob absolute dans overflow-hidden
✅ Texte        → 4 niveaux : white / white/60 / white/40 / white/30
✅ Accent       → 2 couleurs max par palette (+ le fond)
✅ Fonts        → DM Sans, Outfit, Syne, Playfair — jamais Inter/Arial
✅ Coins        → rounded-xl (12px) ou rounded-2xl (16px), jamais moins
✅ z-index      → blobs en z-0, contenu en z-10 obligatoire
```
