# Dark UI — Couleurs Tailwind & Règles d'Usage

---

## RÈGLE UNIVERSELLE DES 3 ACCENTS

```
Accent 1  →  ce que l'œil voit en premier   → titre, CTA, bordure active
Accent 2  →  ce qui guide la lecture         → boutons, labels, icônes
Accent 3  →  l'atmosphère                    → blobs, gradients, hover
```

---

## PALETTES COMPLÈTES

---

### PALETTE 1 — Violet + Cyan (Tech / Dashboard)

```
Fond page    bg-[#0a0a0f]        #0a0a0f
Fond card    bg-[#0d0d14]        #0d0d14
Accent 1     violet-400          #a78bfa    → titres, bordure active, icône
Accent 2     violet-600          #7c3aed    → boutons, CTA
Accent 3     sky-400             #38bdf8    → blobs, hover, gradient
Bordure      border-white/10     rgba(255,255,255,0.10)
Bordure hover border-white/20    rgba(255,255,255,0.20)
```

**Textes**
```
Titre        text-white           #ffffff
Corps        text-white/60        rgba(255,255,255,0.60)
Secondaire   text-white/40        rgba(255,255,255,0.40)
Label        text-white/30        rgba(255,255,255,0.30)
Accent       text-violet-400      #a78bfa
```

**Boutons**
```html
<!-- Principal -->
<button class="bg-violet-600 hover:bg-violet-500 text-white">

<!-- Gradient -->
<button class="bg-gradient-to-r from-violet-600 to-sky-500 text-white">

<!-- Ghost -->
<button class="border border-white/10 hover:border-white/20 bg-white/5 text-white/70">
```

**Dégradés**
```html
<!-- Fond de card — halo haut gauche vers transparent -->
bg-gradient-to-br from-violet-900/40 to-transparent

<!-- Overlay image bas vers haut -->
bg-gradient-to-t from-black/80 via-black/20 to-transparent

<!-- Ligne lumineuse haut de card -->
bg-gradient-to-r from-transparent via-violet-400/60 to-transparent

<!-- Bouton gradient gauche → droite -->
bg-gradient-to-r from-violet-600 to-sky-500
```

**Blobs**
```html
<div class="bg-violet-600 opacity-20 blur-[100px]">  <!-- haut gauche -->
<div class="bg-sky-400    opacity-15 blur-[80px]">   <!-- milieu droite -->
```

---

### PALETTE 2 — Golden (Luxury / Pricing)

```
Fond page    bg-[#0c0900]        #0c0900
Fond card    bg-[#100e00]        #100e00
Accent 1     yellow-400          #fbbf24    → titres, valeurs, bordure
Accent 2     amber-500           #f59e0b    → boutons, labels
Accent 3     orange-400          #fb923c    → blobs, hover, gradient
Bordure      border-yellow-400/20   rgba(251,191,36,0.20)
Bordure hover border-yellow-400/40  rgba(251,191,36,0.40)
```

**Textes**
```
Titre        text-yellow-300      #fde68a
Corps        text-yellow-100/60   rgba(254,249,195,0.60)
Secondaire   text-white/40        rgba(255,255,255,0.40)
Label        text-yellow-400/60   rgba(251,191,36,0.60)
Valeur clé   text-yellow-200      #fef08a
```

**Boutons**
```html
<!-- Principal -->
<button class="bg-amber-500 hover:bg-amber-400 text-black font-semibold">

<!-- Gradient -->
<button class="bg-gradient-to-r from-yellow-400 to-orange-400 text-black font-semibold">

<!-- Ghost -->
<button class="border border-yellow-400/30 hover:border-yellow-400/60 bg-yellow-400/5 text-yellow-300">
```

**Dégradés**
```html
<!-- Fond de card — chaleur haut gauche -->
bg-gradient-to-br from-yellow-900/40 to-transparent

<!-- Fond de card complet -->
bg-gradient-to-b from-yellow-900/30 via-[#100e00] to-[#100e00]

<!-- Bouton gradient gauche → droite -->
bg-gradient-to-r from-yellow-400 to-orange-400

<!-- Overlay luxe diagonal -->
bg-gradient-to-tr from-amber-900/30 via-transparent to-yellow-400/10
```

**Blobs**
```html
<div class="bg-yellow-400 opacity-15 blur-[80px]">   <!-- haut droite -->
<div class="bg-orange-500 opacity-10 blur-[100px]">  <!-- bas gauche -->
```

---

### PALETTE 3 — Sunset (Créatif / Portfolio)

```
Fond page    bg-[#0f0a0a]        #0f0a0a
Fond card    bg-[#140d0d]        #140d0d
Accent 1     pink-400            #f472b6    → titres, CTA, bordure active
Accent 2     orange-500          #f97316    → boutons, labels
Accent 3     yellow-400          #fbbf24    → blobs, hover, gradient
Bordure      border-white/10     rgba(255,255,255,0.10)
Bordure hover border-pink-400/30 rgba(244,114,182,0.30)
```

**Textes**
```
Titre        text-white           #ffffff
Corps        text-white/60        rgba(255,255,255,0.60)
Secondaire   text-white/40        rgba(255,255,255,0.40)
Label        text-pink-400/70     rgba(244,114,182,0.70)
```

**Boutons**
```html
<!-- Principal -->
<button class="bg-pink-500 hover:bg-pink-400 text-white">

<!-- Gradient -->
<button class="bg-gradient-to-r from-pink-500 to-orange-400 text-white">

<!-- Ghost -->
<button class="border border-pink-400/20 hover:border-pink-400/40 bg-white/5 text-pink-300">
```

**Dégradés**
```html
<!-- Fond de card -->
bg-gradient-to-br from-pink-900/30 to-transparent

<!-- Bouton gradient -->
bg-gradient-to-r from-pink-500 to-orange-400

<!-- Fond page ambiance -->
bg-gradient-to-br from-[#1a0a10] via-[#0f0a0a] to-[#0f0800]
```

**Blobs**
```html
<div class="bg-pink-500  opacity-20 blur-[100px]">  <!-- haut gauche -->
<div class="bg-orange-500 opacity-15 blur-[80px]">  <!-- milieu droite -->
<div class="bg-yellow-400 opacity-10 blur-[70px]">  <!-- bas centre -->
```

---

### PALETTE 4 — Emerald (Finance / Crypto)

```
Fond page    bg-[#080f0c]        #080f0c
Fond card    bg-[#0a1410]        #0a1410
Accent 1     emerald-400         #34d399    → titres, valeurs positives, bordure
Accent 2     teal-500            #14b8a6    → boutons, labels
Accent 3     cyan-400            #22d3ee    → blobs, hover, gradient
Bordure      border-emerald-900/50   rgba(6,78,59,0.50)
Bordure hover border-emerald-400/30  rgba(52,211,153,0.30)
```

**Textes**
```
Titre        text-white           #ffffff
Valeur +     text-emerald-400     #34d399
Valeur -     text-red-400         #f87171
Corps        text-white/60        rgba(255,255,255,0.60)
Label        text-emerald-400/60  rgba(52,211,153,0.60)
```

**Boutons**
```html
<!-- Principal -->
<button class="bg-emerald-500 hover:bg-emerald-400 text-black font-semibold">

<!-- Gradient -->
<button class="bg-gradient-to-r from-emerald-500 to-teal-500 text-black font-semibold">

<!-- Ghost -->
<button class="border border-emerald-500/20 hover:border-emerald-500/40 bg-emerald-500/5 text-emerald-400">
```

**Dégradés**
```html
<!-- Fond de card -->
bg-gradient-to-br from-emerald-900/30 to-transparent

<!-- Bouton gradient -->
bg-gradient-to-r from-emerald-500 to-teal-500
```

**Blobs**
```html
<div class="bg-emerald-500 opacity-15 blur-[100px]">  <!-- haut gauche -->
<div class="bg-teal-400   opacity-10 blur-[80px]">    <!-- bas droite -->
```

---

### PALETTE 5 — Mono Violet (SaaS Premium)

```
Fond page    bg-[#0d0b14]        #0d0b14
Fond card    bg-[#110e1a]        #110e1a
Accent 1     violet-400          #a78bfa    → titres, icônes, bordure
Accent 2     purple-500          #a855f7    → boutons
Accent 3     fuchsia-500         #d946ef    → blobs, hover, gradient
Bordure      border-violet-900/50   rgba(76,29,149,0.50)
Bordure hover border-violet-400/30  rgba(167,139,250,0.30)
```

**Textes**
```
Titre        text-white           #ffffff
Corps        text-white/60        rgba(255,255,255,0.60)
Label        text-violet-400/70   rgba(167,139,250,0.70)
Highlight    text-violet-300      #c4b5fd
```

**Boutons**
```html
<!-- Principal -->
<button class="bg-purple-600 hover:bg-purple-500 text-white">

<!-- Gradient -->
<button class="bg-gradient-to-r from-violet-600 to-fuchsia-500 text-white">

<!-- Ghost -->
<button class="border border-violet-400/20 hover:border-violet-400/40 bg-violet-400/5 text-violet-300">
```

**Dégradés**
```html
<!-- Fond de card -->
bg-gradient-to-br from-violet-900/40 to-transparent

<!-- Fond page ambiance -->
bg-gradient-to-br from-[#1a0f2e] via-[#0d0b14] to-[#0d0b14]

<!-- Bouton gradient -->
bg-gradient-to-r from-violet-600 to-fuchsia-500
```

**Blobs**
```html
<div class="bg-violet-600  opacity-20 blur-[100px]">  <!-- haut gauche -->
<div class="bg-fuchsia-500 opacity-15 blur-[80px]">   <!-- bas droite -->
```

---

## RÈGLES DÉGRADÉS — Direction selon l'usage

```
bg-gradient-to-r   → boutons, barres, séparateurs horizontaux
bg-gradient-to-b   → fond de page haut vers bas
bg-gradient-to-br  → halo de coin haut-gauche dans une card ✅ le plus utilisé
bg-gradient-to-t   → overlay sur image (texte lisible en bas)
bg-gradient-to-tr  → halo de coin bas-gauche dans une card
```

---

## RÈGLE OPACITÉ — Pour les couleurs dark

```
Fond blob          opacity-10 à 20   (jamais plus, sinon trop criard)
Fond card accent   /10 à /30         from-violet-900/30
Bordure repos      /10 à /20         border-white/10
Bordure hover      /20 à /40         border-white/20
Label texte        /60 à /70         text-violet-400/60
Bouton ghost fond  /5                bg-white/5 ou bg-violet-500/5
```

---

## GLASSMORPHISME — Recette universelle

```html
<div class="
  bg-white/5
  backdrop-blur-md
  border border-white/10
  rounded-2xl
  shadow-xl shadow-black/30
">
```

> Remplace `bg-white/5` par `bg-violet-500/5` ou `bg-yellow-400/5`
> pour un glass teinté selon ta palette.
