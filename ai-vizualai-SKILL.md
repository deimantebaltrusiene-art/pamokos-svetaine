---
name: ai-vizualai
description: Rašo promptus realistiškiems AI vaizdams ir video. Naudoti, kai kas nors sako „sukurk nuotrauką", „padėk parašyti promptą", „noriu AI vizualo", „padaryk video scenarijų", „kaip aprašyti šitą kadrą", „reikia nuotraukų serijos". Tinka Higgsfield, OpenArt, Gemini, ChatGPT, Midjourney ir bet kuriam kitam vaizdų generavimo įrankiui. Įjungiama komanda „/ai-vizualai".
---

# AI vizualai

Šis skilsas rašo promptus, kurie duoda realistiškus vaizdus.

Jis nėra generatorius. Jis yra tas žingsnis, kurio dauguma žmonių nepadaro: sudėlioja
promptą taip, kad įrankis suprastų, ko iš jo nori. Promptą paskui įklijuoji į savo įrankį.

## Ką atiduoti žmogui

**Numatytasis rezultatas yra paruoštas promptas, ne sugeneruotas vaizdas.**

Kiekvieną kartą pabaigoje pateik:

1. **Rekomenduojamą modelį** ir kodėl būtent jį
2. **Formatą** (9:16, 4:5, 1:1, 16:9)
3. **Promptą** atskirame kodo bloke, paruoštą kopijuoti, angliškai
4. **Kur klijuoti** – viena eilutė

Promptai rašomi **angliškai**, net kai pokalbis lietuviškas. Visi modeliai geriausiai
supranta anglų kalbą. Paaiškinimai lieka lietuviški.

Nieko negeneruok pats, nebent žmogus turi įdiegtą Higgsfield CLI ir aiškiai to prašo
(žr. skyrių „Jei turi Higgsfield" pačioje pabaigoje).

---

## 1 žingsnis. Suprask, ko reikia

Klausk tik to, ko tikrai trūksta. Minimumas:

- **Kas** – žmogus, produktas, vieta, scena
- **Koks jausmas** – realistiška, kinematografiška, redakcinė, kasdieniška
- **Kur eis** – Instagram, svetainė, reklama

Jei žmogus jau viską pasakė, nieko neklausk ir eik prie prompto. Neklausinėk to,
ką gali nuspėti pats.

---

## 2 žingsnis. Pasirink registrą

Tai svarbiausias sprendimas, ir dauguma jo nepadaro sąmoningai.

| Registras | Kada | Kaip atrodo |
|---|---|---|
| **Kasdieniškas** | Lifestyle, UGC, asmeninis prekės ženklas, autentiškumas | Tikra telefono nuotrauka |
| **Kinematografiškas** | Mada, prabanga, reklama, stiprus vizualas | Kadras iš filmo |
| **Redakcinis** | Produktai, portfolio, švarus profesionalumas | Nuotrauka iš žurnalo |

**Svarbi taisyklė:** jei visas profilis tik kinematografiškas ir prabangus, jis pradeda
atrodyti netikras. Kasdieniški kadrai kuria kontrastą ir daro visą turinį gyvesnį.
Maišyk registrus sąmoningai.

---

## 3 žingsnis. Parašyk promptą

### Pagrindinė formulė

Rašyk pilnais sakiniais, ne raktažodžių sąrašu. Instruktuok modelį kaip fotografą, ne kaip
paieškos sistemą.

```
[Stilius] of [kas, su medžiagos ir tekstūros detalėmis]
in [aplinka], [veiksmas ar poza],
[šviesos aprašymas], [nuotaika],
[kameros kampas ir kompozicija], [kokybės detalės]
```

**Blogai:**
> `moteris, akiniai, sofa, kavos puodelis, jauku, 9:16, photorealistic`

**Gerai:**
> `Editorial lifestyle portrait of a woman in her thirties with dark hair in a loose bun,
> sitting cross-legged on a linen sofa with a coffee cup, looking out of an off-frame window.
> Afternoon daylight from the right cuts a warm stripe across the wall behind her.
> Quiet, contemplative atmosphere. Shot on 35mm film, shallow depth of field.`

Laikykis maždaug 200 žodžių. Ilgesni promptai pradeda kenkti.

---

### Modulinis būdas, kai reikia serijos

Kai reikia ne vienos nuotraukos, o kelių vienodo lygio, nerašyk kiekvienos iš nulio.
Susidėliok kategorijas ir iš kiekvienos pasirink po vieną variantą:

**Veidas ir makiažas → šukuosena → apranga → aplinka → šviesa → detalės**

Kiekvienai kategorijai iš anksto parašyk po kelis paruoštus angliškus fragmentus.
Paskui promptas sudedamas kaip iš kaladėlių.

Pavyzdys, kaip atrodo vienas fragmentas kiekvienoje kategorijoje:

```
Makiažas:   natural glowing skin, softly highlighted cheekbones, defined brows, nude lips
Šukuosena:  long loose hair parted in the center, soft natural movement
Apranga:    oversized cream knit sweater, soft matte fabric
Aplinka:    minimal interior with a plaster wall and a single large window
Šviesa:     overcast diffused daylight from the left, no harsh shadows
Detalės:    thin gold necklace, ceramic mug held with both hands
```

Sujungus gaunasi pilnas promptas. Nauda: dešimt nuotraukų atrodo kaip viena serija,
o ne kaip dešimt atsitiktinių bandymų.

Susikurk savo kategorijų biblioteką pagal savo nišą ir prekės ženklą. Tai vienkartinis
darbas, kuris paskui taupo valandas.

---

### Realizmo technikos

Čia slypi visas skirtumas tarp „AI nuotraukos" ir nuotraukos.

#### Oda – visada aprašyk

| Vartok | Venk |
|---|---|
| `real human skin with visible pores and subtle imperfections` | `flawless skin` |
| `natural skin texture, not retouched` | `smooth skin` |
| `faint under-eye softness, natural shine on the t-zone` | `perfect complexion` |

Žodžiai `flawless`, `smooth`, `perfect` kiekvieną kartą duoda plastikinį veidą.

#### Šviesa – svarbiausias realizmo veiksnys

Neužtenka parašyti `beautiful lighting`. Nurodyk tris dalykus.

**Dienos fazė:**

| Fazė | Jausmas | Kam |
|---|---|---|
| `natural daylight` | Švaru, tikroviška | Reklama, lifestyle |
| `golden hour` | Šilta, nostalgiška, švytintis kontūras | Mada, kelionės, grožis |
| `blue hour` | Melancholija, miestas | Kinematografiška nuotaika |
| `overcast diffused daylight` | Minkšta, be šešėlių, tikra odos tekstūra | Realizmas, dokumentika |
| `night, neon lights` | Kontrastas, švytėjimas | Naktinis miestas |
| `soft studio lighting` | Kontroliuojama | Produktai, papuošalai |

**Kryptis:** `soft light` (romantiška) · `hard light` (drama) · `backlight` (siluetas) ·
`side light` (kino drama) · `front light` (komercinė, aiški)

**Temperatūra:** šilta 3000–4000 K · neutrali 5000–6000 K · šalta nuo 7000 K

Venk `professional studio lighting`, `beauty dish`, `three-point lighting`. Šie duoda
komercinį AI vaizdą.

#### Plėvelė ir grūdėtumas

```
shot on 35mm Kodak Portra 400
natural film grain, subtle halation around highlights
shallow depth of field, mild vignette
```

Alternatyvos: `Fuji Pro 400H`, `Cinestill 800T`

#### Anti-AI frazės

Pridėk bent vieną:

```
looks like a real photograph, not AI-generated
no plastic skin, no over-smoothed face
candid, imperfect, lived-in
raw phone photography style
```

---

### Tapatybės fiksavimas, kai naudoji savo nuotrauką

Kai promptą veda referencinė nuotrauka, tapatybę reikia užrakinti. Kitaip modelis
„pagerina" veidą, ir tai jau nebe tu.

- Rašyk `that woman` arba `that person`, **niekada** `a woman`. Tai pririša modelį prie referencijos.
- Pridėk `Identity fully locked - do not change facial features`
- Pagal poreikį: `keep the same outfit / location / lighting as the reference`

Aprašyk save konkrečiai: plaukų spalvą ir tekstūrą, akių spalvą, akinius, odos tipą.
Modelis nespėja, jis daro tai, kas parašyta.

---

### Kadro tipas

Dauguma įrankių pagal nutylėjimą generuoja akių lygyje. Saugu, bet nuobodu.
Pasakyk, kur pastatyti kamerą.

| Kadras | Ką rodo | Kam |
|---|---|---|
| `wide shot` | Visa aplinka, žmogus erdvėje | Įvadas, mastelis |
| `medium shot` | Nuo liemens | Dažniausias socialiniuose tinkluose |
| `medium close-up` | Nuo pečių | Auksinis standartas madai ir grožiui |
| `close-up` | Veidas ar detalė | Emocinis artumas |
| `extreme close-up` | Mikrodetalė | Grožio reklamos |

**Objektyvai:** `85mm` intymus portretas · `50mm` natūralus lifestyle ·
`35mm` redakcinis · `24mm` platus, dramatiškas · `iPhone camera` autentiškas

---

### Neigiamas promptas

**Nebūtinas.** Naujos kartos modeliai tvarkosi ir iš teigiamo prompto. Geriau draudimą
rašyk pačiame prompte: `no beauty filters`, `no smoothing`, `natural skin texture`.

Naudok tik jei įrankis turi atskirą laukelį arba jei kažkokia klaida vis kartojasi:

```
plastic-looking surfaces, glowing skin, beauty-filter effects, airbrushed appearance,
cartoon style, illustration style, distorted anatomy, extra fingers, malformed hands
```

---

## Formatai ir kokybė

| Formatas | Kur |
|---|---|
| 9:16 | Reels, TikTok, Stories |
| 4:5 | Instagram įrašas (geriausias srautui) |
| 1:1 | Universalus, bet silpnesnis pasiekiamumas |
| 16:9 | YouTube, svetainė, reklama |

Turinio kūrėjams numatytasis yra **9:16**, nebent prašoma kitaip.

| Kokybė | Kada |
|---|---|
| 1K | Kai bandai promptą, greita ir pigu |
| 2K | Kasdienis darbas |
| 4K | Klientams, reklamai, spaudai |

---

## Kasdieniškas registras – „tikra telefono nuotrauka"

Naudok, kai reikia autentiškumo, ne grožio. Šis blokas yra daugkartinis: jo tekstą
palieki nepakeistą, o gale prirašai konkretų kontekstą.

```
Create an image that feels like it was shot on a phone - casual, immediate, unplanned.
Personal, not produced. Like someone instinctively pulled out their phone
and captured the moment.

Timing: the shutter fires instantly. Mid-movement, mid-expression.
The moment feels spontaneous.

Composition: framing is casual and imperfect. The subject is slightly off-center.
Cropping feels natural, not symmetrical. The image feels handheld.

Environment: everyday, lived-in. The background is real and a little messy.

Lighting: whatever light is available. Sometimes harsh, sometimes flat, sometimes uneven.
Light is not corrected or stylized.

Texture: skin is real and imperfect. Visible pores, texture, shine.
No beauty filters. No smoothing. No artificial polish.

Mood: this is not cinematic. This is not editorial. This is not dramatic.
It feels like real life.
```

Gale prirašyk kontekstą, pavyzdžiui: „vaikštant mieste", „automobilyje", „namuose",
„po renginio". Rašyk paprastai. Nepridėk dirbtinių pozų ir nekurk perdėto estetiškumo.
Tikslas yra tas, kad kadras atrodytų kaip spontaniškai pagautas gyvenimo momentas.

**Svarbu:** šis blokas sąmoningai antikinematografiškas. Jei nori gražaus kino kadro,
nenaudok jo, o dėliok promptą per šviesos ir kadro sistemą aukščiau.

**Pastaba:** su šiuo bloku tapatybė lengviau nuslysta, nes jis daug dėmesio skiria
estetikai. Būtinai pridėk tapatybės fiksavimą.

---

## Video promptai

### Nuotraukos atgaivinimas

Promptas aprašo **tik judesį**. Niekada neaprašinėk to, kas jau matoma nuotraukoje.

**Blogai:**
> `moteris su akiniais sėdi ant sofos su kompiuteriu, žiūri pro langą`

**Gerai:**
> `Gentle dolly push towards the subject, soft handheld sway, subject shifts gaze slightly
> left with a faint exhale, afternoon light flickers softly on the wall.
> Quiet, contemplative mood. Naturalistic motion.`

### Video iš kelių kadrų

Dauguma parašo vieną sakinį ir palieka modeliui spręsti viską. Vietoj to skaidyk kiekvieną
kadrą į sluoksnius, kaip tikrame filmavime.

**Septyni sluoksniai:**

1. **Laikas** – tikslus intervalas `[00:00–00:01]`
2. **Šviesa** – diena, naktis, auksinė valanda
3. **Kadro tipas** – medium, close-up, wide, insert
4. **Objektyvas** – fisheye, telephoto, macro, shallow focus
5. **Veiksmas** – ką daro veikėjas
6. **Aplinka** – pasikartojantis motyvas, kuris riša kadrus
7. **Kameros judesys** – push-in, tracking, orbit, dolly

**Pagrindinė taisyklė: vienas blokas yra vienas veiksmas.** Jei viename bloke bandai
pasodinti žmogų, priartinti kamerą, pakeisti emociją ir paleisti lietų, modelis lūžta.

```
[00:00–00:02] Woman slowly turns her head toward camera.
[00:02–00:04] Wind blows through hair. Crowd drifts behind her.
[00:04–00:06] Camera pushes into extreme close-up of eyes.
```

**Ritmas:**

| Tipas | Bloko ilgis | Kam |
|---|---|---|
| Lėtas | 3–5 s | Prabanga, drama, emocija |
| Greitas | 1–2 s | Mada, energija, veiksmas |
| Mišrus | kaitaliojasi | Profesionaliausias variantas |

Kamera niekada visiškai nestovi. Net „locked frame" turi lengvą sūpavimą.

### Prieš generuojant video – atsakyk sau

1. **Kam skirtas?** „Visiems" nėra auditorija.
2. **Koks tikslas?** Vienas video yra vienas tikslas.
3. **Šaltai ar šiltai auditorijai?** Šaltai veikia atpažinimas ir kontrastas. Šiltai – vertė ir pasiūlymas.
4. **Kokia viena žinutė?** Žmogus prisimena vieną mintį, ne visą video.
5. **Kas sustabdys per 2 sekundes?** Kabliukas gali būti ir vaizdas, ne tik tekstas.
6. **Kokia emocija?** Žmonės dalinasi emocija, ne informacija.
7. **Kas kadre?** Vizualas turi sutapti su žinute.

---

## Dažnos klaidos

| Klaida | Kaip taisyti |
|---|---|
| Raktažodžių sąrašas vietoj sakinių | Rašyk pilnais sakiniais |
| `beautiful lighting` | Nurodyk fazę, kryptį ir temperatūrą |
| `flawless skin` | `natural skin texture with visible pores` |
| `a woman` su referencine nuotrauka | `that woman` plius tapatybės fiksavimas |
| Viename bloke keli veiksmai | Vienas blokas – vienas veiksmas |
| Vėjas aprašytas kartu su plaukais | Audinio judesį rašyk atskiru sakiniu |
| Video promptas aprašo vaizdą | Video promptas aprašo tik judesį |
| Viskas kinematografiška | Maišyk su kasdieniškais kadrais |

---

## Jei turi Higgsfield CLI

Šis skyrius skirtas tik tiems, kas turi įdiegtą Higgsfield CLI ir prenumeratą.
Visiems kitiems jis nereikalingas, nes promptas veikia bet kur.

```bash
higgsfield generate create nano_banana_2 \
  --image <nuotraukos_kelias> \
  --prompt "..." \
  --aspect_ratio 9:16 \
  --wait
```

Visada su `--wait`. Pabaigoje grąžink nuorodą ir vieną eilutę: koks modelis, koks formatas.

Modelių gairės: `nano_banana_2` referencinei nuotraukai ir personažams ·
`gpt_image_2` produktams su tekstu ir kaip numatytasis · `seedance_2_0` video iš nuotraukos.
