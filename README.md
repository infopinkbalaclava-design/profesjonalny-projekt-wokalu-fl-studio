# Bardzo prosty poradnik: Profesjonalny projekt nagraniowy w FL Studio

Dla: Focusrite + Rode NT1‑A, niski męski głos (rap + śpiew). Tylko stockowe wtyczki FL Studio lub Antares Auto‑Tune Pro (jeśli masz).

Uwaga: wszystko napisane bardzo prosto — krok po kroku.

------------------------------------------------------------
1) Przygotuj pokój (najprościej)
------------------------------------------------------------
1. Znajdź ciche miejsce. Wyłącz klimę, wentylator, zamknij okno.  
2. Połóż duży miękki dywan.  
3. Weź 2–4 grube koce/kołdry:
   - Powieś za mikrofonem (za Twoimi plecami).
   - Powieś po bokach mikrofonu (jak mały namiot).  
4. Szybki trick: otwórz szafę z ubraniami → stań twarzą do środka → mikrofon przed Tobą.  
5. Załóż zamknięte słuchawki. Gotowe.

------------------------------------------------------------
2) Ustaw mikrofon i interfejs (dokładnie)
------------------------------------------------------------
1. Podłącz kabel XLR: Rode NT1‑A → Focusrite wejście 1.  
2. Włącz +48V (phantom) na Focusrite → TAK.  
3. Direct Monitor (na Focusrite) → WYŁ (ważne).  
4. Przykręć pop‑filtr 5–7 cm przed mikrofonem.  
5. Stań 12–20 cm od pop‑filtra (zacznij 15 cm).  
6. Ustaw mikrofon pod kątem ~15–30° (lekko poza osią) — mniej „s” i „ś”.  
7. Śpiewaj/rapuj głośno i ustaw Gain na Focusrite tak, by w FL na kanale było około −12 do −6 dB (nie czerwone).

------------------------------------------------------------
3) Ustawienia FL Studio (dokładnie klikaj)
------------------------------------------------------------
1. Otwórz FL Studio.  
2. Options → Audio settings.  
3. Device: wybierz "Focusrite USB ASIO".  
4. Sample rate: 48000 Hz.  
5. Buffer: ustaw 128 samples (jeśli możesz, 64 dla niższej latencji).  
6. Kliknij "Show ASIO panel" → tu możesz zmieniać bufor jeśli potrzebujesz.

------------------------------------------------------------
4) Jak nagrać wokal (bardzo prosto)
------------------------------------------------------------
1. Naciśnij F9 → otwiera Mixer.  
2. Wybierz Insert 5 (kliknij go).  
3. U góry po prawej: kliknij "IN" → wybierz Mono → Input 1 (Focusrite).  
4. Upewnij się: Direct Monitor na interfejsie WYŁ.  
5. W FL: kliknij czerwone kółko RECORD.  
6. Wybierz: "Audio, into the Playlist as an audio clip".  
7. Naciśnij PLAY (spacja) → śpiewaj/rapuj.  
8. Po skończeniu naciśnij STOP → klip pojawi się w Playlist.  

Uwaga: możesz mieć wtyczki na kanale, żeby słyszeć «na mokro», ale nagrany plik będzie suchy.

------------------------------------------------------------
5) Autotune — Antares Auto‑Tune Pro (jeśli masz) lub stockowe narzędzia FL
------------------------------------------------------------
A) Antares Auto‑Tune Pro (prosty sposób):
1. Na Insert 5 kliknij na wolny slot → wybierz Auto‑Tune Pro.  
2. W ustawieniach:
   - Input Type: wybierz "Low Male" (masz niski głos).  
   - Scale/Key: ustaw skalę piosenki (jeśli nie wiesz → Automatic).  
   - Retune Speed: 
     - Naturalnie: 20–60 ms (gładko).
     - Efekt „hard autotune”: 0–10 ms (szybko, robotycznie).
   - Humanize: 20–50 (dodaje naturalności na długich nutach).  
   - Flex‑Tune: mało lub wyłącz jeśli chcesz ścisłą korektę.  
3. Do ręcznej korekty: włącz Graph Mode → przeciągaj nuty na właściwe wysokości.  
4. Monitoring: słyszysz korekcję na żywo (plugin na insert działa real‑time).

B) Stock w FL (jeśli nie masz Antares)
1. Pitcher (realtime pitch corrector)
   - Wstaw Pitcher na Insert 5.
   - Ustaw Scale/Key = tak jak piosenka.
   - Speed/Correction: ustaw wyżej dla mocniejszej korekcji, niżej (wolniej) dla naturalności.
2. NewTone (edytor, offline)
   - Po nagraniu: kliknij klip → Edit in NewTone.
   - Przeciągaj nuty do prawidłowych wysokości → Export back to playlist.
   - NewTone daje bardzo naturalne poprawki, ale robisz to po nagraniu.

------------------------------------------------------------
6) Prosty łańcuch efektów na wokalu (Insert 5)
------------------------------------------------------------
1) Fruity Parametric EQ 2:
   - High‑Pass: 75–90 Hz.
   - Dołek −1.5 do −3 dB przy 280–350 Hz.
   - Podbicie +1 do +2 dB przy 2.5–3.5 kHz.
   - Małe +0–1 dB przy 10–12 kHz (jeśli trzeba).

2) Maximus (de‑esser):
   - Preset: De‑Esser Wide/Narrow.
   - Crossover High: ~5.5–6 kHz.
   - Threshold → niżej, aż sybilanty są lekko stłumione (2–4 dB redukcji).
   - Release: 50–100 ms.

3) Fruity Compressor:
   - Ratio: 3.5–4:1.
   - Attack: 10–15 ms.
   - Release: 70–100 ms.
   - Threshold: ustaw, by 3–5 dB redukcji na głośnych słowach.
   - Make‑up: +2–4 dB.

4) Drobne „kolorowanie” (opcjonalnie): Fruity WaveShaper / Blood Overdrive bardzo delikatnie (mix 10–20%).

5) Fruity Limiter (opcjonalnie jako gate) — tylko jeśli potrzebujesz odciąć szum.

Wysyłki do efektów:
- Insert 11 = FX_REVERB: Fruity Reeverb 2 → Predelay 15–25 ms, Decay 0.9–1.3 s, Wet na return ~10–15%.  
- Insert 12 = FX_DELAY: Fruity Delay 3 → tempo‑sync 1/8 lub 1/4, Feedback 20–30%, Wet 10–15%.

------------------------------------------------------------
7) Jak ustawić beat, żeby vocal był czytelny
------------------------------------------------------------
1. Poziomy:
   - Ustaw beat tak, by jego główne części były ~−6 do −10 dB (peak) względem wokalu.
   - Wokal: celuj w peak ~−6 dB.  
2. EQ beatu (prosty carving):
   - Na beacie usuń suby poniżej 30–40 Hz (HPF) → czystszy master.
   - Zrób delikatny dołek −1 do −2.5 dB w paśmie 2–4 kHz na beacie, żeby zrobić miejsce na wokal.  
3. Sidechain:
   - Jeśli stopa i bas walczą z wokalem: delikatny sidechain basu do stopy (żeby stopa stała się czystsza).
4. Stereo:
   - Wokal lead zostaw centralnie (mono).
   - Doubles/adliby możesz szeroko rozstawić L/P (Stereo Enhancer +10–30%).
5. Wysyłki FX dla beatu:
   - Używaj tego samego reverb/delay co dla wokalu, ale mniejszy poziom, żeby mix był spójny.

------------------------------------------------------------
8) Jak ustawić odsłuch przy nagrywaniu (żeby było dobrze)
------------------------------------------------------------
1. Focusrite Driver (ASIO) i buffer:
   - Device: Focusrite ASIO.
   - Buffer: 64–128 samples przy nagrywaniu. (Zbyt niskie → trzaski; zbyt wysokie → opóźnienie.)
2. Direct Monitor na interfejsie → WYŁ (żeby nie słyszeć suchego + mokrego naraz).  
3. W FL: wstaw delikatne efekty na Insert 5 (de‑esser, EQ, mały reverb/delay) → będziesz je słyszeć podczas nagrania. Nagranie i tak jest zapisywane „suche”.  
4. Wyłącz ciężkie pluginy (np. konvolvery) podczas nagrania — zwiększają opóźnienie.  
5. Zamknij przeglądarki i inne aplikacje na telefonie/PC → mniej problemów.  
6. Jeśli słyszysz opóźnienie: podnieś buffer (256) aby przetestować stabilność, a potem spróbuj obniżyć ponownie.

------------------------------------------------------------
9) Mastering (prosto)
------------------------------------------------------------
1. Master (Insert 0): Fruity Parametric EQ 2 → Fruity Multiband Compressor → Fruity Limiter.  
2. Fruity Limiter: Ceiling −1.0 dB. Podnoś Gain, ale nie gniotący miks.  
3. Cel loudness (streaming): target ≈ −14 LUFS integrated (dobry standard dla Spotify).  
   - Jeśli nie masz miernika LUFS: staraj się, by RMS refrenu ok. −12 do −10 dB.  
4. Eksport: File → Export → WAV → 24‑bit, 48 kHz, Stereo → Render in high quality.

------------------------------------------------------------
10) Pomysły na krótkie filmiki (shorts / TikTok)
------------------------------------------------------------
- Pokaż 1 trik na film (15–60 s): "Zobacz jak usuwać syk w 10s" (Maximus on/off).  
- Pokaż before/after EQ (5 s before, 5 s after).  
- Pokaż ustawienie mikrofonu: „usta 15 cm, lekko z boku”.  
- Hook w pierwsze 1–2 s: "Chcesz brzmieć pro? Zobacz!".  
- Format: pion 9:16. Duże napisy. #FLStudio #HomeStudio #NT1A.

------------------------------------------------------------
11) Gdzie szukać (dokładne frazy do wpisania)
------------------------------------------------------------
YouTube:
- "FL Studio how to record vocals"  
- "Fruity Parametric EQ 2 tutorial"  
- "Maximus deesser FL Studio"  
- "Auto-Tune Pro tutorial"  
Google:
- "jak wieszać koce na ścianie studio"  
- "Rode NT1‑A Focusrite vocal setup"

------------------------------------------------------------
12) Szybkie wskazówki
------------------------------------------------------------
- Nagrywaj kilka podejść. Zbieraj najlepsze kawałki.  
- Słuchawki zamknięte. Direct Monitor OFF.  
- Monitoruj z efektami, nagrywaj sucho.  
- Jeśli sybilanty: mikrofon poza osią + de‑esser.  
- Zapisz szablon w FL: File → Save as… → Templates.

