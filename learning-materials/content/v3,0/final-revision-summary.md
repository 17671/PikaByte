# Final Revision Summary 
## PikaByte •  
**Module:** Hardware, Networks & Behaviorist AI 
**Sources of feedback:** PentaByte Peer Review + TeamNameNotFound Stage 2 Peer Review 

## Revision Table 

| # | Feedback or problem | Revision and reason | Location and verification | Before / After |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **PentaByte:** Checksum treated as proof of integrity. Matching digit-sum (4729 and 7429 both sum to 22) was presented as proof of no change. | Changed claim to "No change was detected". Added collision activity (4729 ↔ 7429) and discussion distinguishing accidental-error detection from deliberate tampering. Corrects the conceptual error. | Network Security chapter (ready-to-insert section). Verified by constructing the collision. | **Before:** "A matching checksum proves the data has not changed."<br>**After:** "A matching checksum means no change was detected. It does not prove the data is unchanged. Activity: Construct a second number that also sums to 22 (e.g. 4729 and 7429). Discussion: Does this protect against accidental errors, deliberate tampering, or both?" |
| **2** | **NameNotFound (main opportunity) + PentaByte:** Missing intermediate Q-learning worked example. Test Bank Q45 required the full update without a guided trace in the guide. | Added step-by-step worked example breaking the update into target, TD error, scaling by α, and final Q_new. Includes prediction prompt. Supplies missing scaffolding for beginners. | Behaviorist AI chapter, before chapter exercises (ready-to-insert). Arithmetic verified: Q_new = 5.3. | **Before:** (No intermediate example; formula only appeared in the answer key.)<br>**After:** Worked example (Q_old=4, R=6, max Q_next=5, α=0.2, γ=0.9): 1. Target = 10.5 2. TD error = 6.5 3. α × error = 1.3 4. Q_new = 5.3. Prediction prompt included before the steps. |
| **3** | **PentaByte:** MDP definition implied randomness is required, yet a deterministic (probability 1) traffic-light transition was shown. | Added definition note stating transition probabilities may be 0 or 1, deterministic transitions are valid, and learners must distinguish observations from Markov state. Resolves the contradiction. | Behaviorist AI chapter, near first MDP definition (short note prepared). | |
| **4** | **PentaByte (guide pp. 61-62):** Incomplete USB transfer-speed calculation. Example stopped after 12 Mb/s and 480 Mb/s; 5 000 Mb/s result missing. | Added complete prediction-then-reveal table: 600 MB = 4 800 Mb → 400 s / 10 s / 0.96 s. Notes MB vs Mb and why real transfers are slower. Completes the missing result. | Stage 3 → Data Storage Devices in `Markdown_improved.md`. Calculation checked: 4800 ÷ 5000 = 0.96. | **Before:** Calculated only 12 Mb/s (400 s) and 480 Mb/s (10 s).<br>**After:** 12 Mb/s → 400 s \| 480 Mb/s → 10 s \| 5 000 Mb/s → 0.96 s |
| **5** | **PentaByte:** ~95 image insertion cues left as raw placeholders (format readiness). | Converted all 25 placeholders in Stages 1-3 to proper Markdown image syntax with descriptive alt text and `assets/visuals/` paths. Enables rendering once assets are added. | Throughout Stages 1-3 in `Markdown_improved.md`. Verified by search: all `[insert image...]` strings replaced. | |

---

## Before-and-After Evidence for Key Revisions

**#1 - Checksum integrity claim**
*   **Before:** "A matching checksum proves the data has not changed."
*   **After:** "A matching checksum means no change was detected. It does not prove the data is unchanged. Activity: Construct a second number that also sums to 22 (e.g. 4729 and 7429). Discussion: Does this protect against accidental errors, deliberate tampering, or both?"

**#2 - Q-learning scaffolding**
*   **Before:** (No intermediate example; formula only appeared in the answer key.)
*   **After:** Worked example (Q_old=4, R=6, max Q_next=5, α=0.2, γ=0.9): 
    1. Target = 10.5 
    2. TD error = 6.5 
    3. α × error = 1.3 
    4. Q_new = 5.3. 
    *Prediction prompt included before the steps.*

**#4 - USB transfer calculation**
*   **Before:** Calculated only 12 Mb/s (400 s) and 480 Mb/s (10 s).
*   **After:** 12 Mb/s → 400 s | 480 Mb/s → 10 s | 5 000 Mb/s → 0.96 s

**#5 - Image placeholders**
*   **Before:** `[insert image about the four basic functions of a computer...]`
*   **After:** `![Diagram: the four basic functions of a computer...](assets/visuals/placeholder.png)`

---

**Verification method:** 
Peer-review evidence locations cross-checked against the supplied markdown and Stage 2 materials; arithmetic independently recomputed; collision examples constructed by hand; image-syntax conversion confirmed by search. Changes are either applied in `Markdown_improved.md` or supplied as ready-to-insert sections.