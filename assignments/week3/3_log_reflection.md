# Week 3 – AI Interpretation Auditor

## 1. AI Interpretation

The AI interpreted my results as follows:

- **Observation:** Sweetener D has a much higher mean (576.81) than median (167.75).
- **Observation:** Oil B and Pulse C have very similar means and medians.
- **Observation:** All four items have positive first-to-last percentage changes in both cities.
- **Explanation:** The flagged value of 9,999 is increasing Sweetener D's mean significantly.
- **Explanation:** The difference between the mean and median for Staple A could be due to unusually high prices.
- **Claim:** The calculations cannot prove that inflation or production costs caused prices to increase.

Overall, the AI suggested using both the mean and median because unusual values can affect them differently.

## 2. CHECK – Claim Audit

### Colour coding
- Green: Direct observations.
- Amber: Possible explanations.
- Red: Causal claims or unsupported statements.

| AI claim | Colour | How I checked it | Decision |
|---|---|---|---|
| Sweetener D has a much higher mean than median. | Green | Compared the mean and median. | Accept |
| Oil B and Pulse C have similar means and medians. | Green | Compared their calculated values. | Accept |
| All four items have positive percentage changes in both cities. | Green | Checked the percentage change table. | Accept |
| The flagged value of 9,999 increases Sweetener D's mean significantly. | Green | Compared the mean with the flagged value included and excluded. | Accept |
| The difference between the mean and median for Staple A could be due to unusually high prices. | Amber | Compared the mean and median, but cannot confirm the reason from these calculations alone. | Possible explanation |
| The calculations cannot prove that inflation or production costs caused prices to increase. | Green | Checked the information available in the dataset. | Accept |


## 3. CONFUSED CLASSMATE

**AI (Confused Classmate):** I think the mean is always the best measure of a typical price because it includes every observation. Why would we use the median instead?

**Me:** The mean includes every value, but it can be affected by unusually high or low prices. The median is less affected by these values.

**AI (Confused Classmate):** But why does that matter?

**Me:** Because an unusual value can make the mean much higher or lower than most of the actual prices. This can make the mean less representative of a typical observation.

**AI (Confused Classmate):** So is the median always better than the mean?

**Me:** No, not always. Both are useful. It depends on the data and whether there are unusual values.

**AI (Confused Classmate):** Can you give me an example from your results?

**Me:** In Sweetener D, the flagged value of 9,999 increased the mean from 167.15 to 576.81, while the median only changed from 167.50 to 167.75. This shows why looking at both measures is important.
## 4. REFLECT
I learned that the mean and median can give different pictures of the same data. The flagged value had a big effect on the mean but barely changed the median. I also realised that percentage changes do not explain why prices increased. I should be careful about making conclusions without enough evidence.