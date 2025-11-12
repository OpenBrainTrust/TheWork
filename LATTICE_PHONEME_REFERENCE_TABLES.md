# LATTICE PHONEME REFERENCE TABLES

## Patent Documentation: Complete Phonemic Mapping for Tetrahedral Audio Codec

**Document Purpose:** Comprehensive reference tables for labeling lattice diagrams and implementing acoustic synthesis algorithms based on dual tetrahedral geometry.

**Structure Overview:**
- **8 Vertices** (V0-V7): Primary vowel resonators
- **18 Tethers** (T0-T17): Consonant carriers and vowel transitions
- **2 Primary Volumes** (Vol-U, Vol-L): Nasal resonators
- **Geometric Parameters:** R=100 (sphere), r=72 (equator), h=200 (polar diameter)

---

## TABLE 1: VERTEX DATABASE (Vowel Resonators)

| **ID** | **Position (X, Y, Z)** | **Glyph** | **IPA** | **UNLOCK** | **Function** | **F1 (Hz)** | **Type** | **Q** | **Attack (ms)** | **Decay (ms)** | **Sustain** | **Release (ms)** |
|--------|------------------------|-----------|---------|------------|--------------|-------------|----------|-------|-----------------|----------------|-------------|------------------|
| **V0** | (0, 0, +100) | H | /h/ | 8 | EXCITATION_SOURCE | — | Polar | 50 | 10 | 20 | 0.70 | 50 |
| **V1** | (0, +72, 0) | I | /i/ | 9 | SELF_CONSCIOUSNESS | 240 | Equatorial | 150 | 8 | 15 | 0.90 | 40 |
| **V2** | (-62.35, -36, 0) | A | /ɑ/ | 1 | ANIMATION_PRIMAL | 700 | Equatorial | 140 | 6 | 12 | 0.95 | 35 |
| **V3** | (+62.35, -36, 0) | U | /u/ | 21 | HARMONIC_THIRD | 250 | Equatorial | 145 | 9 | 18 | 0.88 | 45 |
| **V4** | (0, 0, -100) | M | /m/ | 13 | CLOSURE_MAGNETISM | — | Polar | 100 | 20 | 30 | 0.85 | 100 |
| **V5** | (0, -72, 0) | E | /e/ | 5 | ENERGY_BALANCE | 500 | Equatorial | 135 | 7 | 14 | 0.92 | 38 |
| **V6** | (-62.35, +36, 0) | O | /o/ | 15 | ORIFICE_PORTAL | 400 | Equatorial | 130 | 10 | 20 | 0.87 | 50 |
| **V7** | (+62.35, +36, 0) | Ə | /ə/ | 37 | CENTER_OF_GRAVITY | 500 | Equatorial | 120 | 5 | 10 | 0.80 | 30 |

**Notes:**
- **F1:** First formant frequency (vowel quality determinant)
- **Q:** Quality factor (resonance sharpness; higher = sustained)
- **UNLOCK:** Energetic function encoding (glyph alpha value)
- **Polar vertices** (V0, V4) serve as excitation/closure points, not sustained vowels

---

## TABLE 2: TETHER DATABASE (Consonant Carriers & Vowel Transitions)

### 2A: UPPER TETRAHEDRON TETHERS (Manifest ▲)

| **ID** | **Path** | **Length** | **Forward IPA** | **Reverse IPA** | **Type** | **Q** | **W-Field κ** | **Fwd Attack (ms)** | **Fwd Decay (ms)** | **Fwd Sustain** | **Fwd Release (ms)** | **Rev Attack (ms)** | **Rev Decay (ms)** | **Rev Sustain** | **Rev Release (ms)** |
|--------|----------|------------|-----------------|-----------------|----------|-------|---------------|---------------------|--------------------|-----------------|-----------------------|---------------------|--------------------|-----------------|----------------------|
| **T0** | V0 → V1 | 123.2 | /hi/ | /ɪç/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T1** | V0 → V2 | 123.2 | /hɑ/ | /ɑx/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T2** | V0 → V3 | 123.2 | /hu/ | /ʊx/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T3** | V1 → V2 | 160.0 | /jɑ/ | /ɑj/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |
| **T4** | V2 → V3 | 160.0 | /ɑw/ | /wɑ/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |
| **T5** | V3 → V1 | 160.0 | /wi/ | /iw/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |

### 2B: LOWER TETRAHEDRON TETHERS (Latent ▼)

| **ID** | **Path** | **Length** | **Forward IPA** | **Reverse IPA** | **Type** | **Q** | **W-Field κ** | **Fwd Attack (ms)** | **Fwd Decay (ms)** | **Fwd Sustain** | **Fwd Release (ms)** | **Rev Attack (ms)** | **Rev Decay (ms)** | **Rev Sustain** | **Rev Release (ms)** |
|--------|----------|------------|-----------------|-----------------|----------|-------|---------------|---------------------|--------------------|-----------------|-----------------------|---------------------|--------------------|-----------------|----------------------|
| **T6** | V4 → V5 | 123.2 | /me/ | /em/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T7** | V4 → V6 | 123.2 | /mo/ | /om/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T8** | V4 → V7 | 123.2 | /mə/ | /əm/ | Polar→Equat | 137 | 0.618 | 10 | 20 | 0.80 | 50 | 15 | 25 | 0.70 | 60 |
| **T9** | V5 → V6 | 160.0 | /ej/ | /je/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |
| **T10** | V6 → V7 | 160.0 | /oə/ | /əo/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |
| **T11** | V7 → V5 | 160.0 | /əw/ | /wə/ | Equatorial | 100 | 0.900 | 5 | 10 | 0.90 | 30 | 5 | 10 | 0.90 | 30 |

### 2C: EQUATORIAL CROSSINGS (Upper ↔ Lower Interface)

| **ID** | **Path** | **Length** | **Forward IPA** | **Reverse IPA** | **Type** | **Q** | **W-Field κ** | **Fwd Attack (ms)** | **Fwd Decay (ms)** | **Fwd Sustain** | **Fwd Release (ms)** | **Rev Attack (ms)** | **Rev Decay (ms)** | **Rev Sustain** | **Rev Release (ms)** |
|--------|----------|------------|-----------------|-----------------|----------|-------|---------------|---------------------|--------------------|-----------------|-----------------------|---------------------|--------------------|-----------------|----------------------|
| **T12** | V1 ↔ V5 | 144.0 | /ie/ | /ei/ | Crossing | 200 | 1.000 | 3 | 5 | 0.95 | 20 | 3 | 5 | 0.95 | 20 |
| **T13** | V2 ↔ V7 | 144.0 | /ɑə/ | /əɑ/ | Crossing | 200 | 1.000 | 3 | 5 | 0.95 | 20 | 3 | 5 | 0.95 | 20 |
| **T14** | V3 ↔ V6 | 144.0 | /uo/ | /ou/ | Crossing | 200 | 1.000 | 3 | 5 | 0.95 | 20 | 3 | 5 | 0.95 | 20 |

**Notes:**
- **Length:** Distance in lattice units (R=100 reference)
- **W-Field κ:** Phase-lock coupling strength (1.0 = perfect coherence)
- **Q:** Tether resonance quality (higher = sustained carrier wave)
- **Equatorial crossings** (T12-T14) have highest Q and κ (optimal energy transfer)

---

## TABLE 3: CONSONANT MAPPING DATABASE

### 3A: PLOSIVES (Node Burst Events)

| **IPA** | **Name** | **Voiced** | **Vertex ID** | **Position** | **Q** | **Attack (ms)** | **Decay (ms)** | **Mechanism** |
|---------|----------|------------|---------------|--------------|-------|-----------------|----------------|---------------|
| /p/ | Voiceless Bilabial | No | V2 | (-62.35, -36, 0) | 8 | 5 | 30 | Sharp node burst → rapid tether excitation → fast extinction |
| /b/ | Voiced Bilabial | Yes | V6 | (-62.35, +36, 0) | 10 | 8 | 40 | Same as /p/ but with lower frequency voicing component |
| /t/ | Voiceless Alveolar | No | V1 | (0, +72, 0) | 7 | 3 | 25 | Sharp node burst → front articulation (tight, fast) |
| /d/ | Voiced Alveolar | Yes | V5 | (0, -72, 0) | 9 | 5 | 35 | Same as /t/ but with voicing component |
| /k/ | Voiceless Velar | No | V0 | (0, 0, +100) | 6 | 8 | 40 | Sharp node burst → back articulation (North Pole) |
| /g/ | Voiced Velar | Yes | V4 | (0, 0, -100) | 8 | 10 | 50 | Same as /k/ but from South Pole (latent excitation) |

### 3B: FRICATIVES (Tether Flow Events)

| **IPA** | **Name** | **Voiced** | **Tether ID** | **Flow Dir** | **Q** | **Attack (ms)** | **Decay (ms)** | **Mechanism** |
|---------|----------|------------|---------------|--------------|-------|-----------------|----------------|---------------|
| /h/ | Glottal | No | T0 | Forward | 20 | 15 | 80 | Turbulent flow from North Pole → UFB (exhale) |
| /s/ | Alveolar | No | T3 | Forward | 35 | 10 | 150 | Turbulent flow along V1→V2 edge (hissing) |
| /z/ | Alveolar | Yes | T3 | Reverse | 40 | 12 | 160 | Same path as /s/ but reverse direction + voicing |
| /f/ | Labiodental | No | T4 | Forward | 30 | 12 | 120 | Turbulent flow along V2→V3 edge (lips/teeth) |
| /v/ | Labiodental | Yes | T4 | Reverse | 35 | 15 | 130 | Same path as /f/ but reverse direction + voicing |
| /ʃ/ | Postalveolar (sh) | No | T5 | Forward | 32 | 14 | 140 | Turbulent flow along V3→V1 edge (broader spectrum) |
| /θ/ | Dental (th-thin) | No | T12 | Forward | 25 | 18 | 100 | Turbulent flow across equatorial crossing V1↔V5 |
| /ð/ | Dental (th-this) | Yes | T13 | Forward | 28 | 20 | 110 | Turbulent flow across equatorial crossing V2↔V7 |

### 3C: NASALS (Volume Resonance Events)

| **IPA** | **Name** | **Volume ID** | **Vertices** | **Q** | **Attack (ms)** | **Decay (ms)** | **Mechanism** |
|---------|----------|---------------|--------------|-------|-----------------|----------------|---------------|
| /m/ | Bilabial | Vol-L | V4, V5, V6, V7 | 100 | 20 | 200 | Full lower tetrahedral volume resonates (lips closed, air through nose) |
| /n/ | Alveolar | Vol-U | V0, V1, V2, V3 | 95 | 18 | 180 | Full upper tetrahedral volume resonates (tongue at alveolar ridge) |
| /ŋ/ | Velar (ng-sing) | Vol-Eq | (sandwich) | 90 | 22 | 190 | Equatorial sandwich volume resonates (back of throat) |

### 3D: LIQUIDS (Special Tether Modes)

| **IPA** | **Name** | **Tether ID** | **Mode** | **Q** | **Attack (ms)** | **Decay (ms)** | **Mechanism** |
|---------|----------|---------------|----------|-------|-----------------|----------------|---------------|
| /l/ | Lateral | T12 | Lateral | 70 | 12 | 100 | Energy flows along tether but radiates perpendicular (lateral articulation) |
| /r/ | Rhotic | T13 | Rotational | 65 | 15 | 110 | Helical energy flow along tether (tongue curl/trill) |

### 3E: GLIDES (Smooth Vowel Transitions)

| **IPA** | **Name** | **Tether ID** | **Q** | **Attack (ms)** | **Decay (ms)** | **Mechanism** |
|---------|----------|---------------|-------|-----------------|----------------|---------------|
| /w/ | Labial-Velar | T4 | 80 | 8 | 60 | Smooth transition along V2→V3 (back rounded articulation) |
| /j/ | Palatal (y-yes) | T3 | 85 | 6 | 50 | Smooth transition along V1→V2 (front articulation) |

---

## TABLE 4: GEOMETRIC PARAMETERS

| **Parameter** | **Symbol** | **Value (units)** | **Ratio** | **UNLOCK** | **Physical Meaning** |
|---------------|------------|-------------------|-----------|------------|----------------------|
| Sphere Radius | R | 100.0 | 1.000 | 100 = THE WORK | Bounding sphere for dual tetrahedron |
| Equatorial Radius | r_eq | 72.0 | 0.720 | 72 = SELF (I AM) | Tetrahedral base radius at Z=0 |
| Polar Height | h_pole | 100.0 | 1.000 | — | North/South Pole distance from origin |
| Polar Diameter | D_pole | 200.0 | 2.000 | 200 = PREGNANT ZERO | Full vertical extent (NP to SP) |
| Equatorial Diameter | D_eq | 144.0 | 1.440 | 144 = LIGHT SQUARED | Full horizontal extent at equator |
| Capacitor Plate Z | Z_cap | ±33.333 | 0.333 | 33 = CENTER LIGHT | W-field equilibration zone |
| Tether (Polar→Equat) | L_PE | 123.2 | 1.232 | — | NP/SP to equatorial base vertex |
| Tether (Equat Edge) | L_EE | 160.0 | 1.600 | 160 = PREGNANT | Free tether span (node surface to surface) |
| Tether (Equat Cross) | L_EC | 144.0 | 1.440 | 144 = LIGHT SQUARED | Upper ↔ Lower crossing tether |
| Node Radiative Radius | r_node | 1.5 | 0.015 | — | Sphere of influence around vertex |
| Aspect Ratio (D_pole/D_eq) | AR | 1.389 | 25:18 | — | Prolate spheroid (Y-on structure) |

**Key Ratios:**
- **L_EE / L_PE ≈ 1.30** (between Perfect Fourth 1.33 and Major Third 1.25)
- **L_EC / L_PE ≈ 1.17** (close to minor second)
- **D_pole / D_eq = 200/144 = 25/18** (ENERGY² / LIGHT²)

---

## TABLE 5: HARMONIC COUPLING MECHANISMS

| **Coupling Type** | **Mechanism** | **Q Range** | **κ Range** | **Direction** | **Function** |
|-------------------|---------------|-------------|-------------|---------------|--------------|
| **Polar→Equatorial** | Excitation/Closure | 130-140 | 0.618 | Manifest ↔ Latent | Initiates/terminates phonation (Perfect Fifth 3:2 transfer) |
| **Equatorial Edge** | Vowel Transition | 95-105 | 0.900 | Bidirectional | Smooth formant transitions (glides, diphthongs) |
| **Equatorial Crossing** | Phase Transfer | 190-210 | 1.000 | Bidirectional | Perfect energy transfer across equator (no loss) |
| **Volume Resonance** | Nasal Cavity | 90-100 | — | Omnidirectional | Full tetrahedral volume excites all 4 faces simultaneously |
| **Face Membrane** | Formant Generator | 50-80 | — | Perpendicular | Triangular drumhead adds harmonic richness (F2/F3 formants) |

**Transfer Ratios:**
- **Manifest → Latent:** Perfect Fifth (3:2) carrier wave
- **Latent → Manifest:** Perfect Fourth (4:3) return wave
- **Equatorial Crossing:** Unity (1:1) perfect coherence

---

## TABLE 6: ADSR ENVELOPE PARAMETER RANGES BY PHONEME TYPE

| **Phoneme Type** | **Attack (ms)** | **Decay (ms)** | **Sustain Level** | **Release (ms)** | **Q Factor** | **Duration Range** |
|------------------|-----------------|----------------|-------------------|------------------|--------------|---------------------|
| **Vowels** | 5-10 | 10-20 | 0.80-0.95 | 30-50 | 120-150 | 50-500 ms |
| **Plosives** | 3-10 | 25-50 | 0.00-0.20 | — | 6-10 | 10-50 ms |
| **Fricatives** | 10-20 | 80-160 | 0.50-0.70 | — | 20-40 | 50-300 ms |
| **Nasals** | 18-22 | 180-200 | 0.85-0.95 | 100-200 | 90-100 | 100-500 ms |
| **Liquids** | 12-15 | 100-110 | 0.60-0.80 | — | 65-70 | 30-150 ms |
| **Glides** | 6-8 | 50-60 | 0.75-0.90 | — | 80-85 | 20-100 ms |

---

## TABLE 7: PHONEME SEQUENCING EXAMPLE (Word: "HOME")

| **Step** | **Time (ms)** | **Element** | **Phoneme** | **Action** | **Energy Flow** |
|----------|---------------|-------------|-------------|------------|-----------------|
| 1 | 0 | V0 (NP) | /h/ | Excite North Pole | Node burst → radiates to V1, V2, V3 |
| 2 | 15 | T7 | /ho/ | Flow NP→LLB | Forward tether excitation (manifest→latent) |
| 3 | 35 | V6 (LLB) | /o/ | Sustain at LLB | Vowel resonance (F1=400 Hz, Q=130) |
| 4 | 135 | T7 | /om/ | Flow LLB→SP | Continue to South Pole (closure) |
| 5 | 155 | V4 (SP) | /m/ | Arrive at SP | Nasal closure (Vol-L resonates, Q=100) |
| 6 | 255 | — | — | Release | Lower tetrahedron volume decays |

**Total Duration:** ≈ 255 ms  
**Path:** V0 → T7 → V6 → T7 → V4 (Vol-L)

---

## TABLE 8: DIAGRAM LABELING NOMENCLATURE

### Vertex Labels (Nodes):
```
V0: NP (North Pole)         H /h/
V1: UFB (Upper Forward)     I /i/
V2: ULB (Upper Left)        A /ɑ/
V3: URB (Upper Right)       U /u/
V4: SP (South Pole)         M /m/
V5: LFB (Lower Forward)     E /e/
V6: LLB (Lower Left)        O /o/
V7: LRB (Lower Right)       Ə /ə/
```

### Tether Labels (Edges):
```
UPPER TETRAHEDRON (▲):
T0: V0→V1 (NP-UFB)    /hi/↔/ɪç/
T1: V0→V2 (NP-ULB)    /hɑ/↔/ɑx/
T2: V0→V3 (NP-URB)    /hu/↔/ʊx/
T3: V1→V2 (UFB-ULB)   /jɑ/↔/ɑj/
T4: V2→V3 (ULB-URB)   /ɑw/↔/wɑ/
T5: V3→V1 (URB-UFB)   /wi/↔/iw/

LOWER TETRAHEDRON (▼):
T6: V4→V5 (SP-LFB)    /me/↔/em/
T7: V4→V6 (SP-LLB)    /mo/↔/om/
T8: V4→V7 (SP-LRB)    /mə/↔/əm/
T9: V5→V6 (LFB-LLB)   /ej/↔/je/
T10: V6→V7 (LLB-LRB)  /oə/↔/əo/
T11: V7→V5 (LRB-LFB)  /əw/↔/wə/

EQUATORIAL CROSSINGS (↔):
T12: V1↔V5 (UFB-LFB)  /ie/↔/ei/
T13: V2↔V7 (ULB-LRB)  /ɑə/↔/əɑ/
T14: V3↔V6 (URB-LLB)  /uo/↔/ou/
```

### Volume Labels:
```
Vol-U: Upper Tetrahedron (V0, V1, V2, V3)  → /n/ (alveolar nasal)
Vol-L: Lower Tetrahedron (V4, V5, V6, V7)  → /m/ (bilabial nasal)
```

---

## USAGE INSTRUCTIONS FOR PATENT DIAGRAMS

**For Clean Diagram Labels:**
1. **Vertices:** Label with ID only (V0-V7) or ID + Glyph (V1:I)
2. **Tethers:** Label with ID only (T0-T14) or ID + IPA (T0:/hi/)
3. **Reference Tables 1-3** for complete parameter details

**For Technical Specifications:**
1. **Cite Table 1** for vertex parameters (position, UNLOCK, Q-factor, ADSR)
2. **Cite Table 2** for tether parameters (length, κ, bidirectional flow)
3. **Cite Table 3** for consonant mapping (mechanism, voiced/voiceless)
4. **Cite Table 4** for geometric constants and ratios

**For Implementation:**
1. **Use Table 5** for coupling mechanism selection
2. **Use Table 6** for phoneme-type parameter ranges
3. **Use Table 7** as sequencing algorithm example
4. **Use Table 8** for consistent nomenclature across documentation

---

## PATENT CLAIMS SUPPORT

**This reference system enables precise claims for:**

1. **Geometric mapping** of phonemes to tetrahedral lattice elements (Tables 1-2)
2. **Bidirectional flow encoding** for tether-based consonants (Table 2)
3. **Volumetric resonance** for nasal phonemes (Table 3C)
4. **UNLOCK-based energetic function** assignments (Table 1, 4)
5. **W-field coupling coefficients** for phase-locked energy transfer (Table 2)
6. **Self-timing phoneme synthesis** from geometric parameters (Table 6-7)
7. **Natural convolution** through face membrane resonance (Table 5)
8. **Perfect geometric ratios** eliminating need for pitch correction (Table 4)

---

**END OF REFERENCE TABLES**

**Document Version:** 1.0  
**Date:** October 28, 2025  
**Authors:** Randy Blain, Jason Blain (Cognitive Code LLC)  
**Patent Application:** GTOS Lattice Audio Codec (Patent #2)

