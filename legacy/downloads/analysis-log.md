# Legacy of Slavery: Contingency Hypotheses


## Purpose

These hypotheses are written before any data is pulled, so each one can fail. The aim is to learn something whichever way the results come out.

The working prior, from lived experience in Georgia: the effects are strong, stand out clearly from background, and have much of the character of frozen accidents. This is recorded as a prior, not a hypothesis, because personal experience may carry selection bias. The tests below are built so that the prior can be wrong.

## Core measurement: the slavery coefficient over time

The main object is β(t): the slavery effect estimated separately for each census decade from 1870 to 2020, on fixed county boundaries. Its shape over time, not any single value, is what tells the models apart.

```latex
Y_c(t) = \alpha_s(t) + \beta(t)\, S_c^{1860} + \gamma(t)^\top G_c + \varepsilon_c(t)
```

Here Y is a county outcome in decade t, S is the 1860 enslaved share of the population, α is a state fixed effect, and G holds geography controls (cotton suitability, rainfall, latitude, river access).

**Null model.** Following Kelly, each β(t) is compared with coefficients from Gaussian random fields matched to the data's spatial correlation length. An estimate counts only if it beats at least 95% of matched noise fields. Moran's I of the residuals is reported every time. The test is also run in reverse, with noise as the outcome.

| Outcome | Rough years available | Likely source |
| --- | --- | --- |
| Black share of population | 1870–2020 | Census via NHGIS |
| Black farm and land ownership | 1900 to present | Census of Agriculture |
| Black literacy, later schooling | 1870 onward | Census full-count microdata (IPUMS) |
| Lynching rate | 1882–1930 | Tolnay–Beck inventory, EJI |
| Black–white income and poverty gap | 1960 onward | Census, ACS |
| Upward mobility | 1978–83 birth cohorts | Opportunity Atlas |
| Small-town business duplication | 1990s onward; earlier from directories | County and ZIP Business Patterns |

Year ranges are approximate and need checking against each source.

## Four competing models

Each model predicts a different shape for β(t) and a different response to shocks. Real history is probably a mix, so the goal is to estimate the weights, not to pick one winner.

| Model | Physics analog | Shape of β(t) | After a barrier-lowering shock |
| --- | --- | --- | --- |
| Decay | Relaxation toward equilibrium | Smooth decline, exponential or power law | Little change; decline was already under way |
| Frozen accident | Quenched disorder | Roughly flat; vanishes once geography is controlled | No response |
| Metastable | Trapped state with Kramers escape | Plateaus broken by steps | Sharp drop timed to the shock |
| Re-forced | Driven system | Rises at critical junctures | Jumps when new forcing is applied |

The key distinction from the Baconton observation: a frozen accident costs nothing to keep. A metastable state costs something every day and persists only because a barrier, such as social sanction, outweighs that cost.

## Hypotheses

Seven hypotheses, each with a stated prediction and a result that would count against it. H6 is speculative and H7 has no predicted direction.

| ID | Hypothesis | Prediction | Counts against it |
| --- | --- | --- | --- |
| H1 | The slavery signal is real, not spatial noise | β(t) for land ownership and the income gap beats 95% of matched noise fields in most decades | Noise matches β(t) in more than 5% of draws |
| H2 | The effect is about slavery, not only soil | β(t) survives cotton-suitability and other geography controls | β(t) collapses with geography controls, meaning a frozen accident of land rather than slavery itself |
| H3 | Change comes in steps (metastability) | Changes in β(t) cluster in decades with barrier-lowering events, such as 1964–65 civil rights law and school desegregation around 1970 | A smooth decay curve fits better than a piecewise step fit, judged by BIC |
| H4 | Re-amplification after Reconstruction | β(t) for lynching, Black voting and land ownership is larger in 1890–1910 than in 1870–1880 | β(t) is flat or falling across those decades |
| H5 | Excess business duplication tracks slavery | In small Southern towns, establishments per capita above the population-scaling expectation rise with 1860 enslaved share | No excess beyond what spatial noise produces |
| H6 | An outside entrant lowers the barrier | After a dollar-store chain arrives, duplicate local businesses close faster in high-duplication towns than in matched towns | No difference in closure rates |
| H7 | Legacy travels with people or stays with places | Linked records compare descendants who left in the Great Migration with those who stayed | Two-sided: convergence among leavers points to place; a persistent gap points to lineage |

## Field note: Baconton, GA

Baconton is the observation that motivated H3, H5 and H6. It's a memory, last checked in person around 2004, and should be treated as a calibration point, not evidence.

- Railroad tracks, never seen in use, divided the small town cleanly in two.
- There were two of nearly everything: gas stations, mini marts and restaurants, in a town remembered as under 2,000 people.
- Joe's grandfather ate lunch at one restaurant almost every day of his life and told Joe never to use the businesses on the other side, even though the food there was better.

**Reading.** The tracks are the quenched part: an old engineering decision that fixed where the line fell. The duplication and the daily lunch choice are the maintained part, a state that cost something every day and lasted anyway.

**Open questions**

- [ ] When did the duplicate businesses close, if they have? Ask family; check Street View history and business directories.
- [ ] Which side was which, and has either side's business closed or changed hands since 2004?
- [ ] What is the town's census population, to check the under-2,000 recollection?

## Where things stand (Nov 6, 2026)

Schooling was the most persistent channel of slavery's legacy: a penalty traceable from Black illiteracy in 1900 to the Black high school gap in 2000, untouched by cotton controls. It ended in a cohort step at school desegregation and has been fading from the adult population as older cohorts age out, leaving a small residual. Land and money outcomes behaved differently: they faded, turned into cotton-economy effects, or reversed. Underneath everything, the demographic map itself is a quenched floor that has held at about half its 1870 strength since 1990.

| Outcome | Period | Slavery effect | Survives cotton and noise? | Shape over time |
| --- | --- | --- | --- | --- |
| Black population share | 1870–2020 | Strong | Yes | Plateau, Great Migration drop, floor at about 0.5 |
| Black farm ownership | 1900–1930 | Strong penalty | Yes to 1920, not 1930 | Shifts from slavery to cotton |
| Black illiteracy | 1900–1920 | Strong penalty | Yes, fully | Slow decay |
| Black high school gap | 1970–2000 | Strong penalty | Yes, fully | Cohort step at desegregation; adult gap 0.21 (1990) to 0.05 (2018–22) |
| College gap | 1970–2000 | Small, growing | Yes | White residents pull ahead |
| Poverty gap | 1990–2000 | Clear penalty | Yes | Roughly halves |
| Black infant mortality | 1917–1941 | None detected | — | Data too weak to tell |
| Black infant mortality | 1960–1972 | Penalty, gone after 1966 | No: a cotton-belt effect | Clean step |
| Black homeownership | 1970–2020 | Reverses to an advantage | Yes | Grows from zero in 1970 |
| Black per-capita income | 2010–2020 | None detected | — | — |

**Against the prior.** The working prior was strong effects with much of the character of frozen accidents. That holds for the demographic floor and for schooling. It does not hold for land, money or health, where the effects were either carried by the cotton economy or changed sign.

**Hypotheses so far.** H1 passes for every outcome except infant mortality and income. H2 separates slavery from soil: schooling and population share are slavery effects; late farm ownership and 1960s infant mortality are cotton-belt effects. H3 has one clean step (infant mortality at 1966), but it belongs to the cotton South. H4 found no re-amplification in 1900–1920. H5–H7 are untested.

**Next.** ACS education and poverty by race for the 2010s; the Opportunity Atlas; home values by race to test the homeownership reversal; formal fits of the four dynamical models to each outcome's curve.

## Fourth result: modern outcomes, 1970–2020

In high-slavery counties the white–Black high school gap stayed about 0.21 per unit of enslaved share from 1970 to 1990 and began narrowing only in 2000. Over the same years the homeownership gap moved the other way and became smaller than elsewhere in the South.

&#91;embedded content: NHGIS 1970 Count 4, 1980 STF 4, 1990 STF 4, 2000 SF 4 and housing time series by race · computed in chat, Nov 6 2026\]

**High school completion, adults 25 and over.** Black completion rose from 26% to 67% between 1970 and 2000, but the gap stayed wide where slavery had been heavy. t ranged from 10.5 to 12.0 against noise thresholds of 3.5–4.3. Cotton controls removed only 2–15% of the effect.

**College.** Black college completion shows no slavery gradient. The white–Black gap is wider in high-slavery counties and growing (β 0.03 in 1970 to 0.06 in 2000), because white residents pull ahead.

**Poverty.** The racial poverty gap was wider in high-slavery counties: β = 0.16 in 1990 (families) and 0.08 in 2000 (adults 18 and over). Both beat noise with cotton controls. The two years use different universes, so the halving is approximate.

**Homeownership reverses.** Black homeownership shows no gradient in 1970, then a positive one that grows to +0.17 by 2020, with the racial gap smaller in high-slavery counties. It survives cotton controls and, at about two-thirds strength, a population density control. Since the same counties have worse schooling and poverty, this is unlikely to be prosperity. Candidate explanations: selective out-migration of renters, very cheap rural housing, and heirs' property. Home values by race would test the second.

**Income, 2010–2020.** Black per-capita income and the Black/white income ratio (about 0.6 everywhere) show no slavery gradient that beats noise with cotton controls. Per-capita figures divide aggregate income by people of all ages, and small-county ACS estimates are noisy.

**Method.** All modern outcomes are on 2020 county boundaries with area-weighted 1860 enslaved shares, state fixed effects, a quadratic in GAEZ cotton suitability, and counties with at least 50 Black residents in the relevant universe.

## Fifth result: schooling ends in a cohort step at desegregation

The slavery penalty in Black high school completion fell by more than half in a single birth cohort: those born 1956–1965, the first to go through school after Southern districts actually desegregated in 1968–1972. Each cohort keeps its value as it ages, so the adult-population gap fell only as older cohorts aged out.

&#91;embedded content: NHGIS 1990 STF 4b and 2000 SF 4 education by age and race · computed in chat, Nov 7 2026\]

**Cohort values.** Born before 1956: β = 0.18–0.22. Born 1956–1965: 0.081 at ages 25–34 (1990) and 0.071 ten years later (2000). Born 1966–1975: 0.058. Pre-desegregation cohorts all beat noise strongly (t of 6.6–9.5); post-desegregation cohorts only marginally (t of 2.8–3.7 against thresholds of 2.7–2.9).

**Adult population, 25 and over.**

| Year | High school gap β | Black high school penalty | College gap β | Poverty gap β |
| --- | --- | --- | --- | --- |
| 1970 | 0.21 | −0.09 | 0.03 | — |
| 1990 | 0.21 | −0.10 | 0.06 | 0.16 |
| 2000 | 0.16 | −0.09 | 0.06 | 0.08 |
| 2008–12 | 0.075 | ≈ 0 | 0.05 | 0.02 (not significant) |
| 2018–22 | 0.050 | ≈ 0 | 0.06 | 0.05 (not significant) |

All with cotton controls. The 2018–22 high school gap (t 3.1 vs 2.2) and college gap (t 3.2 vs 2.7) still beat noise; poverty does not after 2000.

**Physics reading.** Each cohort's schooling is fixed when it passes through school: quenched at formation. The adult population relaxes by turnover, a renewal process, so its time constant is generational replacement, not forgetting. A step in about 1970 therefore appears in the adult stock as a decline stretched over about 50 years, flat until the 1990s and fast after. This is the cleanest barrier-lowering step in the project (H3), and unlike the 1966 infant mortality step it survives cotton controls.

**What persists.** Post-desegregation cohorts still carry about a third of the old penalty (0.06–0.08), and the college gap has not narrowed (0.03 in 1970, 0.06 since 1990). The Black high school penalty itself is gone; the remaining high school gap is white residents doing better in high-slavery counties.

**Caveats.** ACS estimates are noisy for small counties; 2000 and ACS categories differ slightly; a quantitative cohort-replacement model of the adult series is still to do.

## First result: the demographic baseline

Half of the 1860 slavery pattern in where Black Southerners live is still present in 2020: β = 0.51, down from 0.99 in 1870. This is a baseline for later outcomes, not yet a test of the legacy question.

&#91;embedded content: NHGIS county race tables 1860–2020 · computed in chat, Nov 6 2026\]

**Method.** For each decade, county Black population share is regressed on 1860 enslaved share with state fixed effects. The sample is 1,042 counties in the 15 slave states whose county codes persist from 1860. The null is 500 Gaussian random fields with the 1860 map's correlation length of 180 km.

| Model | Long-run floor | Transition | AIC |
| --- | --- | --- | --- |
| Logistic step + floor | 0.49 | Centered 1944, width about 26 years | −132.2 |
| Delayed exponential | 0.17 | Starts about 1898, time constant about 131 years | −132.0 |
| Exponential to zero | 0 | From 1870, time constant about 201 years | −104.2 |

**Status of hypotheses**

- **H1 passes for this outcome.** Real t runs from 26 to 99 across decades; matched noise reaches |t| of 7–9 at its 95th percentile. Naive standard errors mislead: the 1860 map "explains" pure-noise outcomes at p < 0.05 in 61% of draws.
- **H3 is undecided.** The step and slow-decay models fit 1870–2020 equally well and differ only in the future. Annual county estimates by race, about 1990 to now, could separate them.
- Adding a quadratic spatial trend lowers β by at most 0.04 in any decade.

**Limitations**

- The outcome is close to mechanical: formerly enslaved people and their descendants lived where slavery had been. It measures how fixed the demographic map is, not how people fared.
- Counties are matched by code, not boundary, so counties split after 1860 drop out. Shapefiles will fix this.
- No geography controls yet beyond state and spatial trend; cotton suitability is not in.
- Race categories shift: "Colored" in 1870–1890, "Negro" in 1900–1940 and 1960, "Non-white" in 1950, single-race Black from 1970.

## Factoring the coefficient: memory and dynamics separate

The Black population pattern factors into a regional amplitude times a fixed 1860-shaped profile. Most of β's decline before 1970 is the regional amplitude falling, not the profile eroding; since about 1970 the profile itself has been softening when measured proportionally or weighted by population (see Robustness below). Memory lives in the profile; dynamics live in one regional number.

**Anatomy of β.** β is the projection of the year-t county map onto the 1860 map, within states: β = corr × SD(Black share) / SD(1860 enslaved share). It can fall because the pattern scrambles (correlation drops) or because it shrinks in amplitude. A proportional loss of Black population from every county halves β while leaving the shape intact.

| Year | β | Correlation | Average county Black share | β ÷ average share |
| --- | --- | --- | --- | --- |
| 1870 | 0.99 | 0.95 | 30% | 3.31 |
| 1930 | 0.82 | 0.85 | 25% | 3.33 |
| 1960 | 0.70 | 0.77 | 21% | 3.30 |
| 1990 | 0.57 | 0.70 | 18% | 3.23 |
| 2020 | 0.51 | 0.64 | 17% | 3.00 |

The relative imprint (β ÷ average share) held at 3.3 from 1870 to 1990, then fell to 3.0. The falling correlation reflects new structure laid on top, not the slavery component weakening.

&#91;embedded content: NHGIS county race tables 1870–2020; 1,042 counties present in every census · computed in chat, Nov 7 2026\]

**Modes.** Decomposing the 1,042 counties × 16 decades of within-state Black share (SVD):

| Mode | Share of variation | Spatial shape | Time behavior |
| --- | --- | --- | --- |
| 1 | 89% | The 1860 slavery map (correlation 0.88) | Flat to 1910; 0.71 by 1990; 0.66 by 2020 |
| 2 | 6.5% | Suburbs of Southern cities vs rural Black Belt cores | Changes steadily 1880–2000, flat since |
| 3 | 2.5% | Low-slavery counties, likely metros | Out and back: bottoms near 1960, returns by 2020 |

Mode 2's extremes: counties that whitened relative to expectation include Fort Bend and Brazoria TX (Houston suburbs), DeSoto MS (Memphis), Columbia GA (Augusta), Bossier LA, Beaufort SC, and Lee GA, the Albany suburb next to Baconton. Counties that grew relatively more Black include Macon AL, Hancock GA, Williamsburg SC, Jefferson and Claiborne MS, and New Orleans.

**Physics reading.** To about 90%, Black share(county, year) ≈ regional amplitude(year) × 1860 profile(county): separation of variables. The Great Migration acted as a uniform, mean-field loss term, which rescales a profile without reshaping it. Reshaping needs location-specific forces: suburbanization (mode 2, finished around 2000) and return migration into low-slavery metros (mode 3, ongoing). County fates scatter widely, but the scatter averages out within slavery groups: contingent locally, deterministic in aggregate.

**The floor question, restated.** (1) The regional amplitude is not going to zero: the South's Black share has been about 17% since 1980 and is rising. (2) The profile erodes only through location-specific flows, which carry about 9% of the variation over 150 years. The open question is whether return migration into low-slavery metros can flatten a profile that a century of regional drainage left intact. Annual county estimates by race will show it directly.

**Robustness: the frozen shape depends on the observable.** One slavery-shaped mode carries 85–91% of the variation in every version, but whether its shape is frozen does not hold up across versions.

| Version | Mode 1 share | Mode 1 amplitude over time | Least-enslaved fifth ÷ average | Reading |
| --- | --- | --- | --- | --- |
| Shares, counties equal | 89% | 1.0 (1900) → 0.66 (2020) | 0.15 → 0.08 → 0.14 | Shape nearly frozen until 1990 |
| Log shares, counties equal | 91% | 0.73 (1870) → 1.0 (1960–70) → 0.89 (2020) | Log gap −1.91 → −2.26 → −1.86 | Migration sharpened the profile to 1970; softening since |
| Shares, weighted by 1870 population | 85% | 1.0 (1900) → 0.70 (2020), still falling | 0.21 → 0.12 (1960) → 0.49 (2020) | Eroding since 1970 |

In proportional terms the Great Migration sharpened the 1860 profile: low-slavery counties lost Black residents proportionally faster. Since about 1970, Black population growth in low-slavery counties (metros, suburbs, return migration) has been softening it. For where Black Southerners actually live, the population-weighted version is the most relevant, and it shows no floor yet.

**Remaining caveats.** Shares are bounded at 0 and 1; the balanced panel excludes counties created after 1860; a modern-boundary version awaits the remaining decade shapefiles.

## Annual data, 1969–2024: no floor in sight

The relative imprint of slavery on where Black Southerners live has been eroding at an accelerating rate since 1970. The raw coefficient looked like it was leveling off only because the South's regional Black share started rising again after 1990, which masked the erosion. β is still 0.505 in 2024.

&#91;embedded content: SEER US county population 1969–2024 (Census Bureau estimates, bridged race) · computed in chat, Nov 7 2026\]

**Rate of erosion.** The relative imprint (β ÷ average county Black share) fell by 0.02 per decade in the 1970s, 0.06 in the 1980s, 0.12 in the 1990s, 0.13 in the 2000s and 0.18 in the 2010s. Its instantaneous e-folding time shrank from about 830 years (1980) to about 560 (1990), 220 (2000), 190 (2020) and 135 (2024). The log-scale and population-weighted versions accelerate the same way.

**Fits to the relative imprint.** A simple exponential to a floor fails (it cannot bend downward). A compressed exponential with no floor fits well: γ = 2.4, τ = 126 years counted from 1960. Adding a floor improves the fit only slightly and puts it at 1.8 ± 0.3, well below today's 2.75. If a floor exists, the data do not yet see it.

**Two waves, same signature.** The first wave (Great Migration, 1910–1970) drained the South uniformly and left the shape intact; its fit was a compressed exponential with γ = 1.7. The second wave (return migration since 1970) raises the regional Black share but lands disproportionately in low-slavery metros and suburbs, so it erodes the shape; its fit is also compressed, γ = 2.4. Both look like nucleation-and-growth: self-accelerating flows built on migration networks.

**Local examples.** Mitchell County (Baconton): 48% Black in 1970, 48% in 1990, 47% in 2024. Dougherty (Albany): 34% → 51% → 73% as white residents left. Lee County, the suburb next door: 43% → 19% → 28%.

**Caveats.** SEER uses bridged-race Census Bureau estimates (White, Black, Other); counties are weighted equally unless noted; an accelerating decline cannot continue indefinitely, so the fits describe the current regime, not the long-run future.

## Time constants and the floor question

The slavery imprint on where Black Southerners live is still 0.50 today under every model, and that nonzero value is robust: t = 28 against a noise threshold of 7, and 0.43 with cotton controls. What the data cannot yet settle is whether the decline has stopped. This floor-or-no-floor question is now the project's central open question.

| Model of β(t), 1870–2020 | Floor | Time constant | Fit (AIC, lower is better) |
| --- | --- | --- | --- |
| Compressed exponential, γ = 1.7 | 0.46 ± 0.03 | 80 ± 6 years from 1885 | −140 (best) |
| Exponential decay from about 1900 | 0.15 ± 0.14 | 137 ± 34 years | −132 |
| Logistic step | 0.50 ± 0.02 | Width 23 years, centered 1943 | −131 |
| Exponential, no floor | — | About 170 years | −125 |
| Power law, no floor | — | — | −116 |

**Floor and time constant trade off.** Fixing the floor and refitting gives τ = 172 years at a floor of 0, 124 at 0.2, 77 at 0.4 and 49 at 0.5, all with similar fit once the spatially calibrated uncertainty (about ±0.06 per decade, correlated across decades) is respected. The last three decades are still falling, by 0.015–0.03 per decade.

**The exponent.** γ = 1.7 is a compressed exponential: relaxation that accelerates once it starts, as in nucleation-and-growth kinetics or stress-driven relaxation in jammed materials. Glassy systems usually show the opposite (γ < 1). Chain migration fits the compressed form: each departure made the next easier.

**Physics reading.** β(t) is a two-time correlation function: the overlap between the 1860 spatial pattern and the pattern at time t. A plateau would be the non-ergodicity parameter, the fraction of the initial configuration the system cannot forget on accessible timescales.

&#91;embedded content: NHGIS county race tables 1870 and 2020, code-matched counties in former slave states · computed in chat, Nov 6 2026\]

**County fates are not uniform.** For 212 counties with a clear 1870 Black excess, the fraction of that excess left in 2020 is spread almost evenly from 0 to 1.4 (median 0.48). Some counties lost or reversed it; others kept or amplified it (Dougherty, next to Baconton, kept 103%). The smooth aggregate curve averages over very different local histories. Retention before 1970 does not predict retention after 1970 (correlation about 0), which argues against a fixed pinned subset of counties.

**Two readings of the plateau**

- **Dynamical arrest:** the driving force switched off around 1970 when the Great Migration ended and migration turned back toward the South. The remaining pattern then relaxes only by slow diffusion. Predicts continued slow decline.
- **Quenched pinning:** land, heirs' property, churches or kin networks hold the pattern in place. Predicts a flat β.

**Decisive data:** annual county population estimates by race, about 1990 to now. First item for the next session.

## Second result: land and literacy, 1900–1930

In counties with more slavery in 1860, Black farmers owned less of their land and more Black men could not read, and both penalties faded slowly. These are the first outcomes that are not mechanical, and both beat spatial noise in every census year.

&#91;embedded content: NHGIS 1900–1930 agriculture and population tables by race · computed in chat, Nov 6 2026\]

**Reading the sizes.** A Black farmer in a county 60% enslaved in 1860 was about 22 points less likely to own his farm than one in a county with almost no slavery, against an average ownership rate of about 42%. White farmers there also owned less, but by much less. The racial gap shrank from 0.27 to 0.17 over 30 years, a rough relaxation time of 65 years. The illiteracy penalty fell from 0.23 to 0.17, mostly in 1900–1910.

**Infant mortality, 1917–1941: no detectable gradient.** Neither Black nor white infant mortality, nor their ratio, beats spatial noise in any year. This is weak evidence: deaths are counted where they occurred, not where the mother lived; Southern states entered birth registration one by one, so the county sample changes yearly; rural Black births were badly under-registered; and 1934 has a clear data anomaly.

**Hypotheses**

- **H1 now passes for real outcomes:** farm ownership (t of 8.5–10.5 against noise 95th percentile of 5.7–6.3) and illiteracy (t of 12–15 against 3–4).
- **H4 shows no re-amplification in 1900–1920:** the ownership penalty is flat, then falls. The test is weak because race-specific farm data starts in 1900, after Redemption.

**Limitations.** Ownership counts owners plus part owners. The 1900 series uses "colored" operators and 1910–1930 "Negro and other nonwhite". Illiteracy uses native-born men 21 and over in 1900 and men of voting age in 1910–1920. Same code-matching and missing geography controls as the first result.

**Next data:** live births by race for 1959–1972, to pair with infant deaths already in hand and test H3 across hospital desegregation in 1966.

## Third result: a step in infant mortality at 1966

In 1960–1965, Black infant mortality rose with 1860 slavery by 8.5 deaths per 1,000 births per unit of enslaved share. In 1967–1972 the gradient was 0.8 and indistinguishable from noise. The gap closed in one or two years, right after Medicare's 1966 hospital desegregation rules took effect.

&#91;embedded content: NHGIS 1959–1972 vital statistics by race, place of occurrence · computed in chat, Nov 6 2026\]

**Test.** Births-weighted regressions with state-by-year effects, pooled by period, counties with at least 50 nonwhite births. 1960–1965: β = 8.5, t = 5.2 against a noise 95th percentile of 4.3 (noise beats it in 3% of draws). 1967–1972: β = 0.8, t = 0.6. Single years before 1966 mostly sit just under the noise threshold; pooling is what clears it.

**What it means for H3.** This is the first sign of a step: a gradient that held through the early 1960s and vanished within about two years of a barrier-lowering event. It matches Almond, Chay and Greenstone's finding for rural Mississippi. It does not yet rule out other changes in 1965–1967, such as Medicaid or community health centers.

**Limitations**

- **Six states dropped.** In Arkansas, Kentucky, Missouri, Tennessee, Texas and Virginia, white infant mortality is implausibly high until 1967 and normal from 1968, a reporting change rather than a real one. Only the nine states with continuous series are used.
- **Place of occurrence.** As hospital births grew, mothers crossed county lines to deliver. Residence-based rates would be a useful check.
- **Nonwhite, not Black,** before 1970. In these states the two are nearly the same.
- Same code matching and missing geography controls as the earlier results.

## Geography check: boundary-matched slavery shares

Mapping 1860 counties onto 1900, 1930 and 2020 boundaries by area changes no result by more than 0.01. This removes the code-matching limitation listed above.

| Outcome | Years rerun | Counties (code-matched → boundary-matched) | Largest change in β |
| --- | --- | --- | --- |
| Black population share | 1970–2020 | 1,042 → 1,377 | 0.009 |
| Black farm ownership | 1900–1930 | about 900 → about 1,080 | 0.009 |
| White–Black ownership gap | 1900–1930 | about 900 → about 1,080 | 0.011 |
| Black adult male illiteracy | 1900–1920 | about 930 → about 1,130 | 0.004 |

The 1860 enslaved total of 3,950,575 is preserved exactly in every crosswalk. West Virginia, part of Virginia in 1860, now enters the sample. 1910 outcomes use 1900 boundaries and 1920 outcomes use 1930 boundaries. Spatial noise thresholds were recomputed on each geography and every estimate still clears them.

## H2 test: slavery versus cotton soil

Holding cotton suitability fixed, the slavery effect survives in full for literacy and population share, mostly for early farm ownership, and not for 1930 ownership or pre-1966 infant mortality. Slavery and cotton suitability are only moderately related within states (correlation 0.34–0.35), so the two can be separated.

| Outcome | β without cotton | β with cotton | Share kept | Beats noise with cotton? |
| --- | --- | --- | --- | --- |
| Black population share, 1900 | 0.97 | 0.91 | 93% | Yes (t 60 vs 5.6) |
| Black population share, 2020 | 0.50 | 0.43 | 86% | Yes (t 23 vs 5.5) |
| Black adult male illiteracy, 1900 | 0.23 | 0.25 | 107% | Yes (t 15 vs 3.9) |
| Black adult male illiteracy, 1920 | 0.17 | 0.19 | 113% | Yes (t 13 vs 3.9) |
| Black farm ownership penalty, 1900 | 0.38 | 0.30 | 80% | Yes (t 7.8 vs 5.9) |
| Black farm ownership penalty, 1920 | 0.37 | 0.25 | 68% | Yes (t 6.7 vs 5.9) |
| Black farm ownership penalty, 1930 | 0.30 | 0.17 | 55% | No (t 4.6 vs 6.1) |
| White–Black ownership gap, 1930 | 0.17 | 0.09 | 55% | No (t 3.4 vs 4.9) |
| Black infant mortality, 1960–1965 | 8.1 | 3.6 | 44% | No (t 2.0 vs 3.7) |

**Reading it.** The share of the farm-ownership penalty explained by soil rises steadily from 1900 to 1930. By 1930 the ownership gradient looks more like the cotton economy than like slavery as such, which fits the cotton-belt crises of the 1920s. The pre-1966 infant mortality gradient is mostly a cotton-belt pattern too, so the 1966 step in the third result should be read as a step in the cotton South, not yet as a slavery effect.

**Method.** Cotton suitability is the FAO GAEZ agro-climatic potential yield for cotton (1961–1990 climate), averaged over each county and entered as a quadratic. The table uses the low-input version. The high-input version (correlation 0.99 with low-input across counties) keeps slightly more of every effect, 61–95% for ownership and population share, and changes no verdict: 1930 ownership (t 5.2 vs 6.4) and 1960–1965 infant mortality (t 3.4 vs 4.1) still fail the noise test. Paul Rhode has argued GAEZ fits the historical US cotton belt imperfectly, so 1860 cotton production is a planned second control.

## Sixth result (Nov 7): home values explain the homeownership reversal

The Black homeownership advantage in high-slavery counties is cheap ownership, not housing wealth. Black-owned homes there are worth much less relative to white-owned homes in the same county, and higher ownership and lower value cancel almost exactly.

| Outcome, 2018–2022 | β with cotton | t vs noise 95% | Reading |
| --- | --- | --- | --- |
| Black homeownership rate (2020 census) | +0.19 | 8.0 vs 2.6 | Reversal confirmed |
| White–Black homeownership gap | −0.09 | −5.6 vs 2.6 | Gap smaller in high-slavery counties |
| Black ÷ white median home value, same county (log) | −0.41 | −7.0 vs 3.2 | Black-owned homes worth much less relative to white-owned |
| Black median home value (log) | −0.40 | −4.2 vs 4.9 | Not beyond noise in absolute terms |
| Black housing wealth: ownership × value (log) | 0.00 | 0.0 | No gradient: the two cancel |
| Black ÷ white housing wealth (log) | −0.15 | −2.1 vs 2.8 | Not beyond noise |

**Size.** In a county 60% enslaved in 1860, Black-owned homes are worth about 22% less relative to white-owned homes in the same county than in a county with no slavery (exp(−0.41 × 0.6) ≈ 0.78).

**What we thought at the time.** This supports the cheap-housing explanation from the fourth result over a prosperity reading. The legacy in housing moved from whether Black families own to what their homes are worth. It does not separate house quality, location within the county, or appraisal as causes.

**Data and method.** ACS 2018–2022 5-year median value by race of householder (NHGIS ds262); homeownership from the 2020 census tenure-by-race time series. 911 counties with at least 50 Black households and a Black median-value margin of error under 50%. 2020 boundaries, state fixed effects, quadratic cotton suitability, spatial noise null. The 2008–2012 value table was not available in the extract.

## Seventh result (Nov 8): no mobility penalty for children born 1978–1983

For Black children born 1978–1983, growing up in a former high-slavery county shows no detectable penalty in adult income, incarceration, or schooling, compared with Black children from same-income families elsewhere in the same state. The only signal near the noise threshold is that they are less likely to stay in their childhood commuting zone.

| Outcome (Opportunity Atlas, parents at 25th percentile unless noted) | β with cotton | t vs noise 95% |
| --- | --- | --- |
| Black household income rank | +0.012 | 3.1 vs 7.3 |
| Black household income rank, parents at 75th percentile | +0.014 | 2.9 vs 4.8 |
| White minus Black household income rank | +0.009 | 2.1 vs 5.0 |
| Black men, individual income rank | +0.020 | 4.1 vs 5.8 |
| Black men incarcerated in 2010 | −0.014 | −2.4 vs 6.3 |
| Black high school completion | −0.011 | −1.2 vs 4.1 |
| Black college attendance | 0.000 | 0.0 vs 4.2 |
| Black adults still in childhood commuting zone | −0.086 | −5.1 vs 5.2 (−7.1 without cotton) |
| Black income rank among those who stayed | +0.007 | 1.5 vs 6.9 |

**What we thought at the time.** This fits the schooling cohort step: the Black-specific penalty is small or absent for cohorts schooled after desegregation. It also reconciles Berger's finding of lower mobility in high-slavery areas: his measure pooled races, so it mostly reflects racial composition (more Black families, who face the national racial gap everywhere), not an extra penalty tied to the place. The leaving signal matches the accelerating erosion of the population pattern.

**Data and method.** Opportunity Atlas county outcomes (Chetty et al.), children born 1978–1983, by childhood county, race and parental income percentile. Counties with at least 50 children in the group; regressions weighted by group size; 2020 boundaries, state fixed effects, quadratic cotton suitability, spatial noise null. Noise thresholds are higher here than elsewhere because of the weighting.

## Eighth result (Nov 8): the small mobility gap fades from the 1978 to the 1992 cohort

Black children's adult income shows no slavery gradient for either the 1978 or the 1992 birth cohort. The white–Black gap carried a small gradient for children born in 1978, driven by white children doing better in high-slavery counties, and it shrank by about two-thirds by the 1992 cohort, below detection.

| Outcome (Opportunity Atlas trends, cotton controls) | Born 1978 | Born 1992 |
| --- | --- | --- |
| Black income rank, parents at 25th percentile | −0.012 (t −1.0 vs 2.4) | +0.003 (t 0.5 vs 2.5) |
| White minus Black, parents at 25th percentile | 0.038 (t 2.9 vs 2.5) | 0.012 (t 1.9 vs 2.6) |
| Black income rank, parents at 75th percentile | −0.033 (t −1.6 vs 1.9) | −0.003 (t −0.3 vs 2.3) |
| White minus Black, parents at 75th percentile | 0.060 (t 2.7 vs 2.2) | 0.020 (t 1.9 vs 2.4) |
| Change in Black rank, 1978 to 1992 (p25 / p75) | +0.012 / +0.024, not significant |  |

**What we thought at the time.** The post-desegregation residual seen in schooling is not frozen: in mobility it continues to fade across cohorts, more slowly than the desegregation step itself. This revises the fifth result's reading that the residual showed no sign of decline. The 1978 gap only just clears the noise threshold, and these estimates are unweighted, unlike the seventh result's.

**Data and method.** Opportunity Atlas county-level trends in outcomes, 1978–1992 cohorts (Chetty et al.), household income rank by race and parental income percentile; 966 counties in former slave states; unweighted; 2020 boundaries, state fixed effects, quadratic cotton suitability, spatial noise null.

## Ninth result (Nov 8): the stricter cotton control, actual 1860 production

Three results survive controlling for both soil suitability and actual 1860 cotton production: the population map, the schooling penalty, and the Black/white home value gap. Farm ownership, early-1960s infant mortality, and the small 1978 mobility gap do not.

Cells are β (t / noise 95% threshold).

| Outcome | No control | Soil suitability (GAEZ) | 1860 cotton | Both |
| --- | --- | --- | --- | --- |
| Black share 1900 | +0.970 (69.5/7.8) | +0.904 (60.0/6.2) | +0.914 (58.5/7.3) | +0.850 (51.6/4.7) |
| Black share 2020 | +0.504 (28.4/7.1) | +0.428 (22.4/5.2) | +0.454 (22.5/6.7) | +0.382 (18.0/4.2) |
| White–Black farm ownership gap 1900 | +0.277 (10.7/5.5) | +0.214 (7.3/4.8) | +0.108 (3.9/4.0) | +0.053 (1.7/3.9) |
| White–Black farm ownership gap 1920 | +0.231 (9.4/5.1) | +0.168 (6.1/3.9) | +0.119 (4.3/3.9) | +0.063 (2.0/3.5) |
| White–Black farm ownership gap 1930 | +0.164 (6.7/5.4) | +0.086 (3.2/4.8) | +0.101 (3.6/4.6) | +0.021 (0.7/4.5) |
| Black illiteracy 1900 | +0.231 (15.5/3.9) | +0.249 (14.8/4.0) | +0.195 (11.2/3.6) | +0.212 (11.1/3.9) |
| High school gap 1980 | +0.256 (15.2/5.3) | +0.222 (12.0/3.4) | +0.250 (13.2/4.8) | +0.215 (10.6/3.3) |
| High school gap 2000 | +0.181 (12.8/4.5) | +0.159 (10.3/3.5) | +0.149 (9.3/4.6) | +0.130 (7.6/3.4) |
| Black infant mortality 1960–65 | +8.15 (5.4/4.2) | +3.55 (2.0/3.8) | +7.08 (3.7/3.9) | +1.72 (0.8/3.7) |
| Black/white home value 2018–22 (log) | −0.428 (−7.8/2.9) | −0.405 (−6.8/2.8) | −0.310 (−5.0/2.7) | −0.294 (−4.5/2.6) |
| Mobility gap, born 1978 | +0.050 (4.1/2.9) | +0.038 (2.9/2.4) | +0.030 (2.2/2.3) | +0.022 (1.5/2.2) |

**What we thought at the time.** 1860 cotton production correlates more strongly with slavery (0.56) than soil suitability does (0.35), because enslaved labor produced it; controlling for it is conservative and absorbs part of the slavery effect. Results that survive both controls are the core legacy findings. Farm ownership, which looked like a slavery effect through 1920 under soil suitability alone, is mostly a cotton-economy effect from 1900 on; this revises the second result and the H2 test.

**Data and method.** Ginned cotton (400-pound bales) and improved farmland from the NHGIS 1860 agriculture tables (national total 5.38 million bales); intensity = log(1 + bales per 1,000 improved acres), area-weighted onto 1900, 1930 and 2020 boundaries; entered as a quadratic. Otherwise as in the earlier results. 1850 cotton is in hand but not yet used.

## Tenth result (Nov 8): 1850 data — cotton frontier, old vs new slavery, antebellum white schooling

The core results survive a third cotton control (1850 production) and controls for 1850 white schooling. Slavery added during the 1850s predicts later outcomes at least as strongly as slavery already present in 1850, suggesting the legacy tracks intensity at emancipation rather than duration.

Cells are β (t / noise 95% threshold); every spec includes state fixed effects and both 1860-era cotton controls (soil suitability and 1860 production, quadratic).

| Outcome | S (both cotton) | + 1850 cotton | Old: 1850 share | New: 1850–60 increase | + 1850 white schooling |
| --- | --- | --- | --- | --- | --- |
| Black share 1900 | +0.846 (47.7/4.1) | +0.831 (43.6/4.8) | +0.840 (46.6/4.4) | +0.940 (16.1/3.2) | — |
| Black share 2020 | +0.375 (15.5/4.2) | +0.359 (13.8/4.3) | +0.367 (14.9/4.2) | +0.493 (6.4/4.0) | — |
| Farm ownership gap 1900 | +0.060 (1.9/4.1) | −0.043 (−1.3/4.0) | +0.038 (1.2/4.3) | +0.460 (4.5/4.2) | — |
| Black illiteracy 1900 | +0.204 (10.5/3.8) | +0.183 (8.9/3.8) | +0.196 (9.9/4.0) | +0.354 (5.8/3.9) | +0.223 (10.9/3.8) |
| High school gap 1980 | +0.213 (9.6/3.2) | +0.218 (9.2/3.6) | +0.210 (9.3/3.3) | +0.262 (3.8/3.2) | +0.182 (7.8/3.2) |
| High school gap 2000 | +0.139 (7.7/3.3) | +0.142 (7.4/3.4) | +0.137 (7.5/3.3) | +0.175 (3.2/3.0) | +0.118 (6.2/3.3) |
| Black/white home value 2018–22 | −0.273 (−3.9/2.4) | −0.227 (−3.0/2.4) | −0.264 (−3.7/2.3) | −0.435 (−2.0/2.3) | — |

**What we thought at the time.** (1) 1850 cotton adds nothing the 1860 controls missed. (2) No duration dose-response: older slavery does not leave a deeper mark, and the farm ownership gap loads only on the 1850s expansion (newly built boom-era plantations). The legacy looks set by the configuration at emancipation, like a quench, not by time spent in it. This is suggestive only: the 1850 and 1860 shares correlate at 0.986 in counties that existed in both years, so the split rests on little independent variation. (3) The schooling legacy is not inherited antebellum white educational culture: controlling for 1850 white illiteracy and school attendance barely changes it.

**Data and method.** NHGIS 1850 race and slave status, white illiteracy and school attendance, and ginned cotton (3,204,313 enslaved people and 2.47 million bales nationally, matching the census). No 1850 shapefile: 1850 values attach to 1860 counties by code (1,595 of 2,097 match), then are area-weighted onto 1900 and 2020 boundaries; counties need at least 90% of their area covered by 1850 data, which drops most 1850s frontier counties. 1850 cotton = log(1 + bales per 1,000 people), quadratic. White schooling controls = illiterate white adults and white school attenders per white resident.

## Eleventh result (Nov 8): the within-county racial income gap is wider

Black median household income in former high-slavery counties is no lower than in other counties of the same state, but the Black/white income ratio within those counties is substantially lower, and this survives every cotton control. It reverses the earlier null from per-capita income.

Cells are β (t / noise 95% threshold).

| Outcome, ACS 2008–2012 | No control | Soil suitability | 1860 cotton | Both |
| --- | --- | --- | --- | --- |
| Black median household income (log) | −0.150 (−2.6/4.3) | −0.187 (−3.0/3.7) | +0.055 (0.8/3.7) | −0.007 (−0.1/3.4) |
| Black/white median household income (log ratio) | −0.365 (−7.9/3.9) | −0.343 (−6.8/3.1) | −0.290 (−5.5/2.9) | −0.280 (−5.0/2.6) |
| Black/white median family income (log ratio) | −0.350 (−7.3/4.1) | −0.280 (−5.4/3.2) | −0.280 (−5.2/3.3) | −0.224 (−3.9/2.8) |

**Size.** At 60% enslaved, the Black/white household income ratio is about 15% lower than in a county with no slavery (exp(−0.28 × 0.6) ≈ 0.85). The median Black/white ratio across counties is 0.62.

**What we thought at the time.** The earlier income null used aggregate income divided by people of all ages, which was too crude. With proper medians, income joins schooling and home values in a common modern pattern: Black outcomes are similar to Black outcomes elsewhere, but white residents of high-slavery counties do better, so within-county racial gaps are wider. The Opportunity Atlas null for children who grew up there suggests the gap reflects current residents and local economies, possibly selective staying and leaving, more than a disadvantage carried by people from those places.

**Data and method.** ACS 2008–2012 5-year median household and family income by race of householder (NHGIS ds191); counties with a Black margin of error under 50% of the estimate (988 for household, 944 for family). 2020 boundaries, state fixed effects, both cotton controls, spatial noise null. Home values by race for 2008–2012 were not available in NHGIS.

## Twelfth result (Nov 8): 2018–2022 income, inconclusive

Using mean household income by race for 2018–2022, the within-county Black/white income gap shows no slavery gradient, while the 2008–2012 median ratio in the same counties does. The two periods use different measures, so this is not yet evidence that the gap closed.

Cells are β (t / noise 95% threshold).

| Outcome | No control | Soil suitability | 1860 cotton | Both |
| --- | --- | --- | --- | --- |
| Black mean household income 2018–22 (log) | +0.024 (0.4/4.5) | −0.006 (−0.1/4.2) | +0.275 (4.0/4.3) | +0.224 (3.1/3.7) |
| Black/white mean household income 2018–22 (log ratio) | +0.013 (0.3/2.3) | −0.003 (−0.1/2.3) | +0.094 (1.7/2.1) | +0.076 (1.3/2.2) |
| Same 897 counties: 2008–12 median ratio | −0.287 (−6.8/3.9) | −0.268 (−5.9/3.1) | −0.203 (−4.2/3.0) | −0.192 (−3.8/2.7) |
| Same 897 counties: 2018–22 mean ratio | −0.004 (−0.1/2.4) | +0.010 (0.2/2.2) | +0.063 (1.2/2.1) | +0.076 (1.4/2.1) |

**What we thought at the time.** Either the gap closed within a decade, or the measure change drives the difference. Means are pulled up by high earners, which should, if anything, widen a white advantage, so mean versus median alone seems unlikely to erase it. But the 2018–22 means divide ACS aggregate income by 2020 census household counts, and mixing sources adds noise for small Black populations that could blur a real gap toward zero. The clean test is 2018–22 median household income by race.

**Data and method.** ACS 2018–2022 5-year aggregate household income by race of householder (NHGIS ds262) divided by 2020 census households by race (tenure-by-race time series); counties with at least 50 Black households and a Black aggregate margin of error under 50%. Otherwise as in the eleventh result.

## Thirteenth result (Nov 9): 2018–2022 median income resolves the twelfth

With medians in both periods, the within-county Black/white income gap persists in 2018–2022 and may be narrowing slowly. The twelfth result's null came from the mean-based measure.

Cells are β (t / noise 95% threshold).

| Outcome | No control | Soil suitability | 1860 cotton | Both |
| --- | --- | --- | --- | --- |
| 2018–22 Black median household income (log) | −0.153 (−2.4/4.5) | −0.134 (−1.9/4.1) | +0.091 (1.3/3.8) | +0.096 (1.3/3.6) |
| 2018–22 Black/white median income (log ratio), all 911 counties | −0.299 (−5.8/4.0) | −0.237 (−4.3/2.9) | −0.188 (−3.3/2.9) | −0.122 (−2.0/2.6) |
| Same 830 counties: 2008–12 ratio | −0.310 (−7.1/3.9) | −0.268 (−5.7/3.1) | −0.233 (−4.7/3.2) | −0.198 (−3.8/2.9) |
| Same 830 counties: 2018–22 ratio | −0.276 (−5.8/4.0) | −0.222 (−4.3/3.3) | −0.189 (−3.5/3.1) | −0.133 (−2.3/2.5) |
| Same counties: change 2012 → 2022 | +0.035 (0.7/1.9) | +0.046 (0.9/1.9) | +0.043 (0.8/1.9) | +0.065 (1.1/1.9) |

**What we thought at the time.** The gap is real in 2018–2022: it beats noise under each cotton control separately and falls just short only under both together, the most conservative specification. It may be narrowing (about a third smaller under both controls), but the decade's change is not distinguishable from noise. Black median income itself has no gradient in either period. Income remains the softest of the three supports for the modern pattern (schooling, home values, income).

**Data and method.** ACS 2018–2022 5-year median household income by race of householder (NHGIS ds263, Tracts & Larger Areas); counties with Black margin of error under 50%. Same-county comparison restricted to counties passing the filter in both periods. County ratios correlate 0.55 between periods.

## Fourteenth result (Nov 11): Sherman's March leaves no imprint on who lives where

**Why.** This is the first point on an age spectrum of fate built from contingencies of different ages, following the historicity ledger's "test nobody has run." Sherman's March (Nov 1864 – Apr 1865) hit the South just before emancipation, the quench.

**What we did.**

- Built a new panel on 2020 county boundaries: Black count and total population for 1860–1960 (area-interpolated from NHGIS), plus 1969–2024 (SEER).
- Treatment: the march lines traced by Feigenbaum, Lee & Mezzanotti (AEJ: Applied 2022), buffered 5 miles each side, their definition. Coded as any overlap (72 counties) and as the share of county area in the buffer.
- Sample: 277 counties in Georgia, South Carolina and North Carolina within 100 miles of the lines.
- Controls: state fixed effects, 1860 enslaved share, quadratic cotton suitability, and 1860 log population density. Spatial-noise null as before.

**Results.**

- Black share: no year from 1870 to 2024 beats noise. The largest is 1890, −3.0 points (t −3.0 vs. noise 4.5).
- Log population density: 1870 −4% (t −2.1 vs. 2.5), and nothing after.
- A late positive drift in density (2000–2024, t ≈ 1.5) reflects Atlanta-area and coastal growth along the route. It is not significant.

**What we thought at the time.**

- In the residence channel, Sherman's March was a shock that never entered the memory. Its documented effects were on capital (farm values, manufacturing, credit), not on where people lived.
- So it does not yet give a persistence time. That needs farm values per acre by county for 1870–1950, the capital channel. We have only 1860, 1920 and 1930.
- Noise thresholds for Black share in this small three-state sample are high (3–5). Black share is spatially very smooth, so modest effects would be hard to detect here.
- This makes slavery's imprint on the population map look more distinctive. Not every Civil War–era shock to Southern counties left one.

## Fifteenth result (Nov 11): an age spectrum for the residence channel

**Sherman, capital channel.** Added NHGIS county farm value per acre for every census from 1850 to 1959, put onto 2020 counties. Sherman's March: 1870 farm values −11% (t −1.9 vs. noise 3.0). Nothing beats noise in any year. In this cross-sectional design, with a control for 1860 farm value, the march gives no point on the spectrum in any channel.

**Reconstruction officeholders (Logan, JEH 2020).**

- Matched 1,422 Black officials (1867–77) to 1860 counties. Counties created after 1860 were folded into their parent counties. 303 of 887 counties had at least one official.
- Associations are strong and flat for 150 years:
  - Black share +4.6 points in 1870, still +4.1 in 2024, beating noise in most years.
  - Population density +16% in 1870, rising to +38%.
- Read as selection, not effect. Officials marked where freedpeople had gathered by 1870, often in towns. Logan's own identification uses 1860 free Black population as an instrument, which this design does not.

**The 1865–70 resettlement itself.**

- The part of the 1870 Black-share map not predicted by the 1860 map and controls carries about 6% of 1870 variance (sd 5.7 points).
- On all counties, amplitude-adjusted, it falls to about 0.6 by 1960, then recovers to about 0.75 and holds. Over the same years the slavery map's relative imprint goes from 0.95 (1960) to 0.67 (2024).

**Age spectrum.**

- Method: for each census year t0, the innovation is the part of the t0 map not predicted by every earlier map plus controls. I then follow its coefficient in later maps, holding the earlier maps fixed and adjusting for regional amplitude. Each innovation is tested against spatial noise.
- Boundary check. On all counties, the 1890 and 1920 innovations coincide with switches between interpolation shapefiles. So the main run uses 606 counties whose boundaries are unchanged since 1860 (≥95% mutual overlap on 1860, 1900, 1930 and 2020 shapes), with no interpolation.
- Results on stable counties:
  - **1870 innovation:** survival stays about 1.0 for 150 years (0.95–1.22), with no growth-and-decay cycle. Fully remembered.
  - **1890–1940 innovations:** grow to 1.5–1.9 times their size over 30–60 years, then decay.
  - **1950–60 innovations:** grow to about 1.4, then fall to 0.45–0.75 within 60–70 years.
  - **1970–2010 innovations:** grow to 1.7–2.6 and have not yet turned over.
  - Nearly every cell beats noise.

**What we thought at the time.**

- **Not a relaxation spectrum.** Memory in this channel is not monotone decay. Innovations first amplify (momentum: a county that gains Black share relative to expectation keeps gaining) and then decay. That fits the self-reinforcing migration signature (compressed exponentials) and the ledger's missing fourth mechanism, cumulative advantage.
- **Beginnings privileged.** The configuration set right after emancipation is the only innovation that neither amplified nor decayed. This matches the ledger's toy-model signature (frustrated landscape after a quench) and the 1850 split result.
- **Aging is regime-dependent.** At fixed lag, survival depends strongly on t0. Time-translation invariance is broken, but by the migration regime each innovation lived through, not by smooth aging. Innovations made during the Great Migration grew; those made in the 1950s were undone by the return.
- **Caveats.**
  - The innovation mixes real change with census error; error would show as fast decay, which we don't see for 1870.
  - The stable sample is about half the counties and leaves out the fast-changing frontier.
  - Controls for 1860 slavery and cotton apply throughout; amplitude adjustment uses the unweighted county mean.

## Sixteenth result (Nov 11): the 1927 flood enters, leaves, and flips

**What we did.**

- Treatment: Red Cross flooded acres by 1930 county (Hornbeck & Naidu, AER 2014 replication) as a share of county area, area-weighted onto 2020 counties.
- Sample: 549 counties in Arkansas, Louisiana, Mississippi, Tennessee, Kentucky and Missouri; 209 had any flooding.
- Controls: the usual (state fixed effects, 1860 slavery share, cotton suitability), plus pre-flood levels (1920 Black share, 1920 log density, 1925 farm value per acre). Spatial-noise null.

**Results.** Coefficients are for a fully flooded county.

- **Black share:**
  - 1930: −3.7 points (t −4.9 vs. noise 3.4), the documented Black exodus.
  - 1940–1950: about −2.7.
  - 1960: −0.8.
  - 1970: zero.
  - 2000–2024: about +5 points, borderline beating noise in 2010 and 2024.
- **Log population density:** small at first. From 1960 a steady decline, reaching −1.25 log points by 2024 (beats noise from 2010 on).
- **Farm value per acre:** nothing that beats noise.
- Pre-period: density in 1900–1910 was already lower in later-flooded counties (t −3.4, −2.9, under noise), so part of the late decline may be a Delta-wide trend.

**What we thought at the time.**

- **A contingency that decays.** The first shock in the project that clearly entered the residence channel and left it. Black share relaxed with an e-folding time of roughly 25–35 years, much faster than slavery's map and nothing like the frozen 1865–70 resettlement.
- **Then it flipped.** After relaxing, the sign reversed, as homeownership did. One reading follows Hornbeck & Naidu: the flood pushed Delta agriculture to mechanize, the region later depopulated, and white residents left faster. The memory of the shock was carried forward by the capital channel and resurfaced in the residence channel with the opposite sign.
- **For the age spectrum.** A shock of age about 97 years, with fast decay and a sign reversal. The survival curves don't stay positive. Memory can change sign, which a relaxation spectrum cannot represent.

## Prior work and sources

The existing literature mostly reports a single 1860-to-today regression. What is new here is the time-resolved β(t), the noise tests, and the business-duplication measure.

| Work | What it gives this project |
| --- | --- |
| [Acharya, Blackwell & Sen, *Deep Roots* (2018)](https://www.iq.harvard.edu/news/using-data-map-political-legacy-slavery-how-blackwell-and-sen-won-2019-apsa-prize) | Slavery share predicts white racial attitudes today; claims re-forcing after Reconstruction (tests H4) |
| [Kelly, "The Standard Errors of Persistence" (2019)](https://cepr.org/publications/DP13783) | The spatial-noise null model used in every test |
| [Kelly, "Understanding Persistence" (2020)](https://researchrepository.ucd.ie/handle/10197/11538) | Robustness checks; effect sizes often halve against spatial trends |
| [Berger, "Places of Persistence" (2018)](https://link.springer.com/article/10.1007/s13524-018-0693-4) | Slavery predicts lower upward mobility today |
| [Collins & Holtkamp, NBER w33860](https://www.nber.org/system/files/working_papers/w33860/w33860.pdf) | Black men's mobility into property ownership, 1870–1900, lowest in cotton counties |
| [Bleakley & Ferrie, QJE (2016)](https://econpapers.repec.org/RePEc:oup:qjecon:v:131:y:2016:i:3:p:1455-1495.) | Georgia's 1832 land lottery: persistence rate of a one-time wealth shock, for comparison |
| [Ananat, AEJ: Applied (2011)](https://econpapers.repec.org/RePEc:aea:aejapp:v:3:y:2011:i:2:p:34-66) | Railroad layouts as a source of segregation; the urban version of Baconton |

**Data to request** (needs a free account, then attach here): NHGIS county tables and boundary crosswalks, IPUMS full-count censuses and linked records, Census of Agriculture by race, Opportunity Atlas, and County and ZIP Business Patterns.
