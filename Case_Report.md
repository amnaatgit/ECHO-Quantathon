# ECHO — Case Report
### An echo, not a voice

**Investigator:** Amna Shahzad (Roll No. CT_24018, Section B, AI) · Entangled Minds: The Quantathon · Qubits Qrew, NED University · 20 October 2026

**Evidence:** `ECHO_Investigation_Notebook.ipynb` (this repository). Mandatory modules 01, 03, 05; declared stretch module 06; additional stretch modules 02 and 04. All six reached Gold.

## 1. Verdict

**ECHO never sent a message. Dr. Zara Mahmud mistook an *echo* (a correlation shared by two detectors) for a *voice* (a signal travelling between them). That mistake was her own. But the experiment around it was shaped by someone else: its "random" trigger was a tuned coin, and the record of the night was edited afterwards.**

| Question | Our answer | Confidence |
|---|---|---|
| Could ECHO send a message faster than light? | **No.** Bob's results never depend on what Alice does, and teleportation delivers nothing without two classical bits. | **High (~95%)**: measured, and proven exactly |
| Did Zara fool herself? | **Yes, on the physics.** She tested agreement in only one basis, and she counted a hidden classical channel as "nothing crossing". | **High (~85%)** |
| Did someone help her believe it, and make sure it ran? | **Probably.** The seed was tuned to exactly 30%, evidence of an observer was deleted, and Bilal's warning disappeared. | **Moderate (~65%)** |
| Who? | **Leading suspect: Sana Rao.** Every gap in the records sits inside her access. **Strongest alternative: Prof. Vance** planted the seed. | **Low to moderate** (Sana ~45%, Vance ~30%, nobody ~20%, other ~5%) |
| What happened to Zara? | **Unknown.** "No exit logs" proves nothing when the same records were edited. | Open question |

## 2. The three clues that decided it

1. **Agreement is not communication (M03 + M06).** A pre-agreed secret reproduces Zara's "always agree" data exactly: 100% agreement in the Z basis. Only a second basis tells them apart. In the X–X setting the entangled pair agrees 100% of the time and the secret only 51%; on the CHSH test the pair scores S = 2.80, above the classical limit of 2. Yet *whatever Alice does*, Bob's detector stays at P(0) = 0.49–0.51, and his exact state is the maximally mixed I/2. Teleportation succeeds 100% of the time with two classical bits, and 50% without them, which is 0.00 bits of information. **The detectors could agree; they could never talk.**
2. **The "random" seed was a loaded coin (M02).** Ry(1.159) gives P(1) = sin²(0.5795) = 0.300. We measured 0.303 ± 0.020, which is 17.6σ from a fair coin (p ≈ 10⁻⁷⁰). The number 1.159 is *exactly* the angle that produces 30% (2·asin√0.3 = 1.1593), so it was chosen, not the result of drift. A fair coin would need 1.571. Zara "trusted it completely", so it was most likely set by someone else.
3. **A recorded result never changes when it is read again (M04).** Measuring twice gives the same answer in 100% of shots, while gates on their own can always be undone. So a log that "changed when it was observed" changed at its *first* observation: during the run, by someone who was present. It did not change when investigators later read it (ARIA's account), and it was not "corrupted" (Sana's account).

*Supporting evidence:* her recovered last word (M05) is **ECHO**, which reads naturally as her own verdict on the experiment.

## 3. Evidence board

| FACT (observed) | CLAIM (stated by someone) | INFERENCE (ours) | OPEN QUESTION |
|---|---|---|---|
| Z basis: entangled pair 100% agree; shared secret 100% agree | Zara: the detectors are "linked across space" | Her data cannot tell entanglement apart from a shared secret | Did she ever measure in a second basis? |
| X–X: pair 100%, secret 51%; CHSH S = 2.80 vs 1.44 | Zara: teleported "with no qubit ever crossing the gap" | True, but two classical bits crossed, inside the machine | — |
| Bob's P(0) = 0.50 for every action Alice takes; ρ_B = I/2 | Vance: "ECHO was never real" | He is right about the physics, which is not evidence of his innocence | Did Vance know about the seed? |
| Teleportation: 100% with 2 bits, 50% with 0 bits | ARIA: "No unauthorised command was issued" | An authorised command can still be dishonest: the configuration was manipulated | Who configured ARIA's seed, and when? |
| Seed P(1) = 0.303 ± 0.020; the angle encodes exactly 30% | ARIA: the investigators corrupted the log | M04 contradicts this: re-reading cannot change a recorded result | Which seed outcome triggered ECHO? |
| A re-measurement returns the same value 100% of the time | Sana: "I only deleted a corrupted log" | A mid-run measurement *looks* like corruption, so deleting the log erased the trace of an observer | Was the deleted log the same one that "changed"? |
| Last word = "ECHO" (20 of 32 triples repaired) | Bilal: "I warned her. Nobody listened." | His warning matches what we found; the disappearance of his report counts in his favour | What did his report say, and who removed it? |
| *(Case file)* No exit logs; a log deleted; a report missing | — | All three gaps fall inside one person's access (Sana's) | Where is Zara? |

## 4. Experiments and results
*(Circuits and histograms are in the notebook; key figures are in the Appendix.)*

| Mod. | Purpose | Gates / circuit | Prediction | Result | What it proves |
|---|---|---|---|---|---|
| 01 | Learn the machine's language | X; H; H·H; X on q0 and q2 | 1; 50/50; 0; `101` | 1.000; 0.491; 2000/2000 `0`; 2000/2000 `101` | Something that looks random can hide a certain answer |
| 02 | Test the trigger | H coin; the recovered Ry(1.159), unchanged | 500 ± 16; P(1) = 0.300 | 498/1000 (fair); 0.303 ± 0.020; 5σ needs 157 shots | The seed is a tuned 70/30 coin |
| 03 | Test the "link" | H+CNOT vs measure-then-CNOT; H before readout; CHSH | Z basis: both 100%; X basis: 100% vs 50%; Bob unaffected | 100/100; 100/51; Bob 0.49–0.51; S = 2.80 vs 1.44 | Correlation, never communication |
| 04 | Test "changed when observed" | XHH, HXH, mid-circuit measurement, re-measurement | 1; 0; 50/50; unchanged | 1.000; 0.000; ≈0.5; 100% identical; rulebook correct on 120/120 sequences | Only the first measurement erases |
| 05 | Recover the message | Majority vote; 3-qubit bit-flip code (CNOT + Toffoli) | ≤ 1 flip per triple is corrected | "ECHO"; with 2 flips it reads "DCHO"; qubit code 100% for 1 error, ~70% for 2 | Corrects 1 flip, notices 2; qubits can't be cloned |
| 06 | Test the teleportation claim | Recovered circuit with/without corrections; ρ_B | 100% / 50%; ρ_B = I/2 | 100% / 50%; I/2 for all 5 messages; 1.00 vs 0.00 bits of information | No faster-than-light signal: 2 classical bits are required |

## 5. Interpretation

**The physics settles the crux.** Zara's evidence, perfect agreement in one basis, is exactly what a shared secret produces. The experiment that would have told them apart (a second basis) appears nowhere in her claims. Even if her pair *was* truly entangled, as our X–X and CHSH results show such a pair would be, entanglement only correlates: Bob's statistics are blind to anything Alice does. Her "teleportation with no qubit crossing" is genuine teleportation, but it works only with two classical bits. In a single machine those bits travel through the classical control lines (the `if_test` corrections), where nobody would think of them as "crossing the gap."

**The human evidence is weaker, and we label it as inference.** That the seed is tuned is a fact; that someone else chose it is an inference. Module 04 turns the statements by ARIA and Sana from neutral into suspect: neither "the investigators corrupted it" nor "a corrupted log" fits how measured records actually behave. And the three gaps in the record (the missing exit logs, the deleted log, Bilal's missing report) all point to the one person with full access to the records. **Access gives opportunity, not motive**, which is why our confidence about *who* stays below 50%.

**What our evidence cannot prove:** who set the seed angle, why they did it, or what happened to Zara. *Physics proves what ECHO could not do. It cannot prove who made it look as if it could.*

## 6. Alternative explanation

**Honest self-deception, with nobody else involved.** In this version Zara chose the 70/30 seed herself (for example, to make ECHO fire on a schedule), the deleted log really was corrupted, and Bilal's report was simply lost. It is the strongest competing theory, because it needs no villain and it fully explains why the physics failed.

**Why we prefer our theory:**
1. The case file says she *trusted* the seed. You don't "trust" a number you tuned yourself.
2. The angle is accurate to 30%, which is the signature of a deliberate choice.
3. "Corrupted" does not match how a measured record behaves (M04).
4. Three independent gaps in the record, all inside one person's access, are unlikely to be coincidence.

**Within the foul-play theory, Prof. Vance is the strongest rival suspect.** He had a motive (to be proven right by letting ECHO "succeed" on a rigged trigger, then exposing it) and the knowledge to choose 1.159. But he had no access to the records, so on his own he cannot explain the deleted log or the missing report.

## 7. Next experiment

**A forensic audit of ARIA, plus recovery of the deleted log:**
- **(a)** Pull ARIA's configuration history for the seed parameter.
- **(b)** Compare the machine's own run time (unlocked in M01) with ARIA's timestamps and with the time of Sana's deletion.
- **(c)** If ARIA stores logs redundantly, the way Zara's message was stored (M05), recover the "corrupted" log by majority vote.

| Check | Expected if our theory is right | Expected if it was honest self-deception |
|---|---|---|
| Seed history | Changed from a fair value (π/2) to 1.159 by an account other than Zara's, shortly before the run | Set to 1.159 by Zara's own account from the start |
| Timestamps | The machine's time ≠ ARIA's logged time | The times match |
| Recovered log | A clean record of a mid-run measurement (an observer was present) | Genuine noise |

**Physics follow-up:** run the CHSH test from M03 on real IBM hardware. We expect S > 2 (somewhat below 2.83, because of noise), with Bob's results still 50/50: the entanglement is real, and the signalling is still zero.

## 8. Limitations

- **Ideal simulator.** All results come from a noise-free simulator. Hardware noise would change the numbers, but noise cannot create signalling.
- **M03's gate set has limits.** With only H, X and CNOT we can rule out a simple shared coin, but not every possible local strategy. The CHSH bonus (which needs `ry`) covers that, but only in simulation: Bell-test loopholes (locality, detection) can't be closed here.
- **M02 has an unknown.** We don't know which seed outcome fired ECHO, so we can show the seed was rigged, but not which way it pushed the firing.
- **Human conclusions rest on the case file.** Our human-side conclusions depend on the case file's statements. Physics identifies what is impossible; it does not identify people.

## 9. References & AI / external assistance

- Qiskit SDK 2.6 and Qiskit Aer 0.18: IBM Quantum documentation; source at github.com/Qiskit.
- J. Watrous, *Basics of Quantum Information*, IBM Quantum Learning (teleportation, the CHSH game).
- M. A. Nielsen & I. L. Chuang, *Quantum Computation and Quantum Information* (teleportation, no-cloning, the 3-qubit bit-flip code).
- J. F. Clauser, M. A. Horne, A. Shimony & R. A. Holt, *Phys. Rev. Lett.* **23**, 880 (1969): the CHSH inequality.
- W. K. Wootters & W. H. Zurek, *Nature* **299**, 802 (1982): the no-cloning theorem.
- Qubits Qrew: *Hello Quantum* warm-up deck, the ECHO Participant Manual, and the ECHO starter notebook.
- **AI assistance:** I used an AI assistant (Claude, Anthropic) substantially: to explain concepts, structure the notebook, and draft code and the wording of this report. Every number comes from running the notebook. I checked each prediction against the output and can explain every circuit.

---

## Appendix: supplementary figures *(not counted toward the page limit)*

![M03 basis test](figures/m03_basis_test.png)
*Figure A1 (M03 Gold): a second measurement basis separates real entanglement from a pre-agreed secret.*

![M06 accuracy](figures/m06_accuracy.png)
*Figure A2 (M06 Gold): the message arrives only when the classical bits arrive. With 0 bits, every message is a coin toss.*

![M02 seed](figures/m02_seed.png)
*Figure A3 (M02 Silver): the recovered seed Ry(1.159) is a 70/30 coin.*

![M06 teleport](figures/m06_teleport.png)
*Figure A4 (M06 Bronze): the recovered teleportation circuit. The two `If` blocks are the classical channel.*

![M05 quantum code](figures/m05_qcode.png)
*Figure A5 (M05): the 3-qubit bit-flip code protects a superposition from a single error without copying it.*

![M01 silver](figures/m01_silver.png)
*Figure A6 (M01 Silver): H·H, "looks uncertain but is secretly certain".*
