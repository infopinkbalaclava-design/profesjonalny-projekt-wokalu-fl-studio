# Bardzo prosty poradnik: Profesjonalny projekt nagraniowy w FL Studio

Poradnik dla konfiguracji z Focusrite i Rode NT1‑A, przeznaczony do nagrywania niskiego męskiego głosu (rap + śpiew). Zakłada użycie stockowych wtyczek FL Studio lub Antares Auto‑Tune Pro (jeśli posiadasz).

Uwaga: instrukcje są napisane krok po kroku, w prosty i praktyczny sposób.

---

## 1) Przygotowanie pokoju (najprościej)

1. Wybierz ciche miejsce: wyłącz klimatyzację, wentylator i zamknij okna.  
2. Połóż duży, miękki dywan na podłodze.  
3. Użyj 2–4 grubych kocy/kołder:
   - Powieś je za mikrofonem (za plecami).  
   - Powieś po bokach mikrofonu, tworząc mały „namiot” akustyczny.  
4. Szybki trik: otwórz szafę z ubraniami, stań twarzą do środka, ustaw mikrofon przed sobą — to proste tłumienie odbić.  
5. Załóż zamknięte słuchawki (closed‑back). Gotowe.

---

## 2) Ustawienie mikrofonu i interfejsu (dokładnie)

1. Podłącz kabel XLR: Rode NT1‑A → wejście 1 w Focusrite.  
2. Włącz zasilanie +48 V (phantom) na interfejsie.  
3. Wyłącz Direct Monitor na Focusrite (ważne przy nagrywaniu z monitorowaniem w DAW).  
4. Zamocuj pop‑filtr 5–7 cm przed mikrofonem.  
5. Stań 12–20 cm od pop‑filtra (zalecane ~15 cm).  
6. Ustaw mikrofon pod kątem ~15–30° względem osi ust (lekko poza osią) — pomaga to zmniejszyć sybilanty („s”, „ś”).  
7. Śpiewaj/rapuj w normalnej głośności i ustaw Gain na Focusrite tak, aby w FL Studio poziom na kanale był około −12 do −6 dB (unikaj clippingu i czerwonego pola).

---

## 3) Ustawienia FL Studio

1. Otwórz FL Studio.  
2. Options → Audio Settings.  
3. Device: wybierz "Focusrite USB ASIO".  
4. Sample Rate: ustaw 48000 Hz.  
5. Buffer: ustaw 128 samples (dla mniejszej latencji możesz ustawić 64, ale sprawdź stabilność).  
6. Kliknij "Show ASIO panel", aby zmienić ustawienia bufora w razie potrzeby.

---

## 4) Jak nagrać wokal (prosto)

1. Naciśnij F9, aby otworzyć Mixer.  
2. Wybierz Insert 5 (lub inny wolny Insert).  
3. W prawym górnym rogu kliknij "IN" → wybierz Mono → Input 1 (Focusrite).  
4. Upewnij się, że Direct Monitor na interfejsie jest WYŁĄCZONY.  
5. W FL Studio włącz nagrywanie (czerwone kółko RECORD).  
6. Wybierz: "Audio, into the Playlist as an audio clip".  
7. Naciśnij PLAY (spacja) i nagrywaj.  
8. Po zakończeniu nagrania naciśnij STOP — nagrany klip pojawi się na Playlist.

Uwaga: możesz dodać wtyczki na kanale, żeby słyszeć efekt „na mokro” podczas nagrania, ale sam zapisany plik pozostanie suchy (bez efektów insertów, jeśli monitorujesz przez DAW zależnie od ustawień).

---

## 5) Autotune — Antares Auto‑Tune Pro (jeśli masz) lub stockowe narzędzia FL

### A) Antares Auto‑Tune Pro (szybki sposób)
1. Na Insert 5 dodaj Auto‑Tune Pro.  
2. Ustawienia:
   - **Input Type**: wybierz "Low Male".  
   - **Scale / Key**: ustaw skalę utworu (jeśli nie znasz — Automatic).  
   - **Retune Speed**:
     - Naturalne: 20–60 ms.  
     - Efekt „hard autotune”: 0–10 ms (szybkie „robotyczne” korekty).  
   - **Humanize**: 20–50 (dodaje naturalności przy długich nutach).  
   - **Flex‑Tune**: ustaw nisko lub wyłącz, jeśli chcesz ścisłą korektę.  
3. Do precyzyjnej korekty użyj Graph Mode — przeciągaj nuty.  
4. Monitoring działa w czasie rzeczywistym (plugin na insercie).

### B) Stock w FL Studio
1. **Pitcher** (real‑time pitch corrector):  
   - Dodaj Pitcher na Insert 5.  
   - Ustaw Scale/Key zgodnie z utworem.  
   - Speed/Correction: wyższe wartości → mocniejsza korekcja; niższe → naturalniej.  
2. **NewTone** (offline):  
   - Po nagraniu: kliknij klip → Edit in NewTone.  
   - Przesuwaj nuty do poprawnych wysokości → Export back to playlist.  
   - NewTone daje naturalne, precyzyjne poprawki, ale robisz to po nagraniu.

---

## 6) Prosty łańcuch efektów na wokalu (przykład na Insert 5)

1. **Fruity Parametric EQ 2**:  
   - High‑Pass: 75–90 Hz.  
   - Dołek: −1.5 do −3 dB przy 280–350 Hz (usuń „mulistość”).  
   - Podbicie: +1 do +2 dB przy 2.5–3.5 kHz (czytelność).  
   - Opcjonalnie: +0–1 dB przy 10–12 kHz (powietrze).  

2. **Maximus** (de‑esser lub dedykowany de‑esser):  
   - Preset: De‑Esser Wide/Narrow.  
   - Crossover High: ~5.5–6 kHz.  
   - Threshold: obniż do lekkiej redukcji sybilantów (2–4 dB).  
   - Release: 50–100 ms.  

3. **Fruity Compressor**:  
   - Ratio: 3.5–4:1.  
   - Attack: 10–15 ms.  
   - Release: 70–100 ms.  
   - Threshold: ustaw tak, aby uzyskać ~3–5 dB redukcji na głośniejszych frazach.  
   - Make‑up gain: +2–4 dB.  

4. Delikatne „kolorowanie” (opcjonalnie): Fruity WaveShaper lub Blood Overdrive — bardzo subtelnie (mix 10–20%).  
5. **Fruity Limiter** (opcjonalnie jako gate) — tylko jeśli trzeba odciąć niepożądany szum.

Wysyłki do efektów (returns):  
- Insert 11 = FX_REVERB: Fruity Reverb 2 → Predelay 15–25 ms, Decay 0.9–1.3 s, Wet na return ~10–15%.  
- Insert 12 = FX_DELAY: Fruity Delay 3 → tempo‑sync 1/8 lub 1/4, Feedback 20–30%, Wet 10–15%.

---

## 7) Jak ustawić beat, żeby wokal był czytelny

1. Poziomy:
   - Beat: główne elementy ustaw na ~−6 do −10 dB (peak) względem wokalu.  
   - Wokal: celuj w peak ~−6 dB (mały zapas przed limitowaniem).  
2. EQ beatu (prosty carving):
   - Usuń suby poniżej 30–40 Hz (HPF) na beacie.  
   - Zrób delikatny dołek −1 do −2.5 dB w paśmie 2–4 kHz na beacie, aby zrobić miejsce dla wokalu.  
3. Sidechain:
   - Jeśli stopa i bas „kłócą się” z wokalem, zastosuj delikatny sidechain lub obniż zakresy kolidujące z wokalem.  
4. Stereo:
   - Lead vocal pozostaw w centrum (mono).  
   - Doubles i adliby możesz szerzej rozstawić L/P (Stereo Enhancer +10–30%).  
5. FX beatu: stosuj reverb/delay podobny do tego, co używasz dla wokalu, lecz na niższym poziomie, aby spójność była zachowana.

---

## 8) Odsłuch podczas nagrywania

1. Sterowniki i bufor:
   - Device: Focusrite ASIO.  
   - Buffer: 64–128 samples przy nagrywaniu (zbyt niski → trzaski, zbyt wysoki → opóźnienie).  
2. Direct Monitor: wyłączony (żeby nie słyszeć jednocześnie suchego i mokrego sygnału).  
3. W FL: włóż delikatne efekty na Insert 5 (de‑esser, EQ, lekki reverb/delay) — będziesz ich słyszeć na monitoringu. Nagranie i tak zapisze się „suche”.  
4. Wyłącz ciężkie pluginy (konwolvery itp.) podczas nagrania — zmniejszy to opóźnienia.  
5. Zamknij niepotrzebne programy (przeglądarki, aplikacje na telefonie/PC).  
6. Jeśli słyszysz opóźnienie, zwiększ bufor (np. 256) aby sprawdzić stabilność, potem spróbuj zmniejszyć ponownie.

---

## 9) Mastering (prosto)

1. Na masterze (Insert 0) użyj kolejno:  
   - Fruity Parametric EQ 2 → Fruity Multiband Compressor → Fruity Limiter.  
2. Fruity Limiter: ustaw Ceiling na −1.0 dB. Podnoś gain, ale nie miażdż miksu.  
3. Cel loudness (streaming): target ≈ −14 LUFS integrated (dobry punkt dla platform typu Spotify).  
   - Jeśli nie masz miernika LUFS: dąż do RMS refrenu około −12 do −10 dB.  
4. Eksport: File → Export → WAV → 24‑bit, 48 kHz, Stereo → Render in high quality.

---

## 10) Pomysły na krótkie filmiki (shorts / TikTok)

- Pokaż 1 trik (15–60 s): np. "Jak usuwać syk w 10 s" (Maximus on/off).  
- Before/after EQ (5 s before, 5 s after).  
- Ustawienie mikrofonu: „usta 15 cm, lekko z boku”.  
- Hook w pierwsze 1–2 s: "Chcesz brzmieć pro? Zobacz!".  
- Format: pion 9:16, duże napisy. #FLStudio #HomeStudio #NT1A

---

## 11) Gdzie szukać (przykładowe frazy)

YouTube:  
- "FL Studio how to record vocals"  
- "Fruity Parametric EQ 2 tutorial"  
- "Maximus de‑esser FL Studio"  
- "Auto‑Tune Pro tutorial"

Google:  
- "jak wieszać koce na ścianie studio"  
- "Rode NT1‑A Focusrite vocal setup"

---

## 12) Szybkie wskazówki

- Nagrywaj kilka podejść i wybieraj najlepsze fragmenty.  
- Używaj zamkniętych słuchawek. Direct Monitor OFF.  
- Monitoruj z efektami, nagrywaj sucho.  
- Przy sybilantach: ustaw mikrofon poza osią + użyj de‑esser.  
- Zapisz szablon w FL: File → Save as… → Templates.

---

## Kreatywne dodatki — pomysły do eksperymentów 

1. Warstwa „tekstury” z głosu:
   - Nagraj krótkie szumy, szept lub dźwięki ustami (10–20 s). Zrób pitch‑shift w dół, dodaj LPF, rozciągnij w czasie (time‑stretch) i użyj jako ambientowej podkładki pod refren. Daje to unikalne, organiczne tło.

2. Reverse reverb vocal (efekt dramatyczny):
   - Skopiuj krótki fragment wokalu, odwróć go (reverse), dodaj długi reverb, wyrenderuj, odwróć ponownie — wstaw przed oryginalną frazą jako „lead‑in” (efekt rozbłysku przed słowem).

3. „Vocal chop” jako instrument:
   - Wytnij krótki hook (sybilki, samogłoski), złóż na MIDI (sampler) i zagraj nimi melodię. Możesz dodać formant shift, filtrowanie i delay synced do tempa.

4. Lo‑fi resampling trick:
   - Eksportuj fragment wokalu, zmniejsz bit-depth, dodaj bitcrusher i EQ, ponownie załaduj do projektu jako tekstura. Mieszaj na niskim poziomie, żeby dodać charakteru.

5. Harmonizer / formant play:
   - Duplikuj ścieżkę wokalu, przesuwaj subtelnie pitch (±2–6 semitones) i formant, ustaw lekki delay/panning — otrzymasz naturalne harmonikacje bez wyraźnego efektu „chipmunk”.

6. Szybki preset „hook”:
   - Stwórz Insert Template: EQ (HP 80 Hz) → De‑esser → Compressor (fast) → Auto‑Tune (light) → Send to short reverb + sync delay. Zapisz jako preset, używaj do szybkiego przygotowania wokalu do nagrań.

7. Mini‑wyzwanie kreatywne (15 minut):
   - Wybierz 1 linijkę tekstu, nagraj 5 podejść: normalnie, szeptem, krzykiem, z falsetem, i z warstwą „vocal chop”. Wybierz 2 najlepsze i połącz. To często rodzi złote fragmenty.

---

## Checklista przed eksportem (szybkie 10 punktów)

- [ ] Gain staging: nie ma clippingu.  
- [ ] Wokal czytelny w miksie (spróbuj na małych głośnikach).  
- [ ] Sybilanty pod kontrolą.  
- [ ] Reverb/delay spójne między wokalem a beatem.  
- [ ] Automatyka (volume) tam, gdzie potrzeba.  
- [ ] Master nie jest przepalony (headroom ~ −1 dB przed limiterem).  
- [ ] LUFS sprawdzone (target ~ −14).  
- [ ] Eksport ustawiony: WAV 24‑bit 48 kHz.  
- [ ] Nazewnictwo plików jasne: utwor_v1_final.wav.  
- [ ] Zapisz projekt i stwórz backup.
