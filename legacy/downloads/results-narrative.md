# The Shape of a Legacy: Results Narrative (Draft)


## Two of everything

My mother's family has a farm outside Baconton, a small town in Mitchell
County, in southwest Georgia. Railroad tracks run through the middle of
it. I never saw a train on them, but they divided the town cleanly in
two, and the town kept two of nearly everything: two gas stations, two
mini marts, two restaurants, in a town of well under two thousand
people. My grandfather ate lunch at one of those restaurants almost
every day of his life, and he told me never to go to the businesses on
the other side. The food over there was distinctly better. I knew that
for sure, but I don't know whether he ever ate there to find out before
he died.

I grew up near Atlanta hearing people argue about how much the legacy of
slavery still shapes life in the South. Some said it was everywhere;
others said it was long gone. What struck me, coming back to the
question years later with a background in physics, is that this is not
only a moral argument. It is an empirical one about memory: how long a
system remembers a shock, through which channels, and whether that
memory decays, holds, or gets renewed.

This project tries to measure that memory directly. It asks how strongly
a Southern county's condition today, and in every census year since
emancipation, can be predicted from how many of its people were enslaved
in 1860; and then what the *shape* of that prediction over time tells us
about what kind of memory it is.

The answer, so far, is that there is not one legacy but several, each
with its own dynamics. Where Black Southerners live still follows the
1860 map strongly, though that pattern is now eroding at an accelerating
rate. Schooling carried the largest penalty for over a century and then
broke in a single generation at desegregation. Land and health tell
different stories again: those penalties turned out to belong to the
cotton economy rather than to slavery itself. And today the legacy has
changed form. Black residents of former high-slavery counties now do
about as well as Black residents elsewhere, but white residents there do
better, so racial gaps in income, home values, and schooling stay wider
in exactly the places slavery was heaviest.

## How to weigh a legacy

The central measurement is simple. For each census year, I compare
counties within the same state and ask: if one county was 30 percentage
points more enslaved than another in 1860, how different are they in
year *t*? That slope is the **slavery coefficient**, β. A β of 1 for an
outcome measured in shares means the 1860 difference survives
one-for-one; a β of 0 means it has vanished. The 1860 enslaved share
comes from the census (the national total reproduces the 3.95 million
enslaved people recorded that year), mapped by area onto later county
boundaries.

Three safeguards matter more than the regression itself.

- **Spatial noise.** Maps of the South are smooth: neighboring counties
  resemble each other in soil, rivers, and history. Smooth maps can
  produce impressive-looking correlations by accident. Following the
  economist Morgan Kelly, every estimate is tested against hundreds of
  artificial random maps with the same spatial smoothness. A result
  counts only if the real slavery map beats 95% of the fakes. This is
  not a formality: the 1860 map is smooth enough that it "significantly"
  predicts pure noise most of the time under naive statistics.

- **Cotton.** Slavery concentrated where cotton grew best, so any
  slavery effect might really be a soil effect. Every result is rerun
  holding fixed two measures of cotton: the FAO's estimate of each
  county's agro-climatic suitability for cotton, and the county's actual
  cotton production in 1860. The second is deliberately conservative,
  since enslaved people produced that cotton and controlling for it
  absorbs part of the slavery effect; results that survive both are the
  core findings. A third check adds 1850 cotton production, to capture
  the cotton frontier of the 1850s.

- **Time.** Instead of a single comparison between 1860 and today, β is
  measured in every census decade from 1870 to 2020, and annually from
  1969 to 2024 for population. The shape of β over time, not any single
  value, is what distinguishes a legacy that decays from one that is
  frozen or renewed.

The data come from the IPUMS National Historical GIS (county census
tables 1860–2022), the National Cancer Institute's SEER county
population series (1969–2024), and FAO crop suitability rasters.

## The map that won't let go

The most basic legacy is where people live. In 1870, five years after
emancipation, β for Black population share was 0.99: freed people lived
almost exactly where they had been enslaved. In 2024 it is still 0.505.
A county that was 60% enslaved in 1860 is, on average, about 30 points
more Black today than a county in the same state with almost no slavery.
This holds against spatial noise by a wide margin and survives the
cotton controls.

<img src="../figures/static/fig01_beta_population_1870-2020.png"
style="width:6in;height:2.90178in"
alt="Figure 1 · NHGIS county race tables 1860–2020" />

Figure 1 · NHGIS county race tables 1860–2020

The fall from 0.99 to 0.5 looks at first like a slow forgetting. It is
mostly something else. The coefficient can shrink in two ways: the 1860
pattern can scramble, or it can keep its shape while shrinking in
amplitude. Dividing β by the South's average Black share separates the
two, and that ratio barely moved from 1870 to 1990. Sorting counties
into five groups by 1860 slavery and dividing each group's Black share
by the regional average, the curves collapse almost perfectly for 150
years: the most-enslaved fifth stays at 2.1–2.3 times the average
throughout. A single spatial mode shaped like the 1860 map carries 89%
of all county-by-decade variation.

<img src="../figures/static/fig02_data_collapse_quintiles.png"
style="width:6in;height:2.98214in"
alt="Figure 2 · NHGIS county race tables 1870–2020; 1,042 counties present in every census" />

Figure 2 · NHGIS county race tables 1870–2020; 1,042 counties present in
every census

The Great Migration, then, did not erase the map. It drained the whole
South at roughly the same per-capita rate everywhere, shrinking the
pattern without reshaping it. In the language of physics, it acted like
a uniform loss term, which rescales any profile without changing its
shape.

Reshaping came later, and it came from the return. Since about 1970,
Black migration has run back toward the South, but it lands
disproportionately in metros and suburbs that had little slavery. The
South's Black share has risen, while the relative imprint of the 1860
map has eroded at an accelerating rate: 0.02 per decade in the 1970s,
0.18 in the 2010s. Its e-folding time has shrunk from roughly 800 years
in 1980 to about 135 years today. The raw coefficient seemed to level
off around 0.5 only because the rising regional share masked the erosion
underneath. On the annual data there is no floor in sight.

<img src="../figures/static/fig03_relative_imprint_1969-2024.png"
style="width:6in;height:2.98214in"
alt="Figure 3 · SEER US county population 1969–2024 (Census Bureau estimates, bridged race)" />

Figure 3 · SEER US county population 1969–2024 (Census Bureau estimates,
bridged race)

Both waves have the same mathematical signature: a compressed
exponential, a decline that accelerates once it starts (exponents of 1.7
and 2.4). That is the signature of self-reinforcing flows, consistent
with migration networks in which each move makes the next one easier.

The regional curve is smooth, but county fates are not. Across counties,
the share of the 1870 Black excess still present in 2020 is spread
almost evenly from none to all, and some counties amplified it. Mitchell
County, where Baconton sits, was 48% Black in 1970, 48% in 1990, and 47%
in 2024. Next door, Dougherty County, around Albany, went from 34% to
73% as white residents left, many for Lee County, which went from 43% to
19% and back to 28%. The aggregate looks almost law-like precisely
because it averages over many contingent local histories.

## What the map carried: land, letters, and schools

Where people live matters because of what comes with the place. Two
channels stand out in the historical record.

**Land.** Between 1900 and 1930, Black farmers in counties with heavy
1860 slavery were far less likely to own the land they worked. A Black
farmer in a county 60% enslaved in 1860 was about 22 points less likely
to own his farm than one in a county with almost no slavery, against an
average ownership rate near 42%. White farmers there owned less too, but
by much less. The racial gap narrowed slowly, with a relaxation time on
the order of 65 years. But the cotton controls change the reading.
Holding soil suitability fixed, the ownership gap looks like a slavery
effect through 1920. Holding actual 1860 cotton production fixed as
well, it shrinks to a fifth of its size and no longer beats spatial
noise, even in 1900. Land ownership looks less like a direct memory of
slavery than like a memory carried by the cotton plantation economy and
the tenancy system that replaced it.

**Letters.** Black adult illiteracy in 1900–1920 was sharply higher
where slavery had been heavier, and that effect survives both cotton
controls almost completely. It is also not an inherited antebellum white
educational culture: controlling for white illiteracy and school
attendance in 1850 barely changes it. Schooling is the channel where the
legacy behaves most like slavery itself rather than like soil.

<img src="../figures/static/fig04_land_literacy_1900-1930.png"
style="width:6in;height:2.90178in"
alt="Figure 4 · NHGIS 1900–1930 agriculture and population tables by race" />

Figure 4 · NHGIS 1900–1930 agriculture and population tables by race

**Schools.** That schooling penalty continued, almost unchanged in size,
through the twentieth century. The white–Black high school completion
gap in the adult population was about 0.21 per unit of 1860 slavery in
1970, 1980, and 1990, even as Black high school completion rose from 26%
to 58%. Then it fell: 0.16 in 2000, 0.075 in 2008–2012, 0.05 in
2018–2022.

The census age tables show why. Broken down by birth cohort, the gap is
about 0.19 for everyone born before 1956, and then it drops by more than
half, to 0.06–0.08, starting with people born 1956–1965. That cohort
entered first grade between 1962 and 1971 and went through high school
in the 1970s, just after the court orders of 1968–1972 that forced
Southern school districts to actually desegregate. Each cohort keeps its
value as it ages: the 1956–1965 cohort measures 0.08 in 1990 and 0.07 in
2000.

<img src="../figures/static/fig05_schooling_cohort_step.png"
style="width:6in;height:2.98214in"
alt="Figure 5 · NHGIS 1990 STF 4b and 2000 SF 4 education by age and race" />

Figure 5 · NHGIS 1990 STF 4b and 2000 SF 4 education by age and race

So the century-long schooling penalty ended in a single generational
step. It looked like a slow decline in the adult population only because
the older, segregated cohorts take decades to age out. It did not reach
zero. Post-desegregation cohorts still carry about a third of the old
penalty, and the college gap has not narrowed since 1990. What remains
is no longer a deficit in Black high school completion, which has no
slavery gradient today, but an advantage for white residents of
high-slavery counties.

## What faded, moved, or flipped

Not every outcome carries a slavery signal, and some of the
clearest-looking ones dissolve under scrutiny.

**Infant health.** In the early 1960s, Black infant mortality ran higher
in former high-slavery counties, by roughly 8 deaths per 1,000 births
per unit of 1860 slavery. After 1966, when Medicare's rules forced
Southern hospitals to desegregate, that gap closed within about two
years. It is the sharpest step anywhere in the data. But it does not
survive the cotton controls: the pre-1966 penalty belongs to the cotton
South in general, not to slavery specifically. For 1917–1941 the data
are too incomplete to say anything.

**Poverty.** The white–Black poverty gap was wider in high-slavery
counties in 1990 and 2000, then fell below detection by 2008–2012.

**Income.** Black households in former high-slavery counties earn about
the same as Black households elsewhere in their state. But the racial
income gap within those counties is substantially wider: in 2008–2012,
in a county that was 60% enslaved in 1860, Black median household income
relative to white was about 15% lower than in a county with no slavery,
and this survives every cotton control. White households there do
relatively better. The gap persists in 2018–2022, though it may be
narrowing slowly: in the same counties it shrank by about a third under
the strictest cotton controls, a change too small to distinguish from
noise, and under those controls the 2018–2022 gap only just misses the
noise threshold. Income is the softest of the modern gaps.

**Mobility.** The most direct test of a living legacy is whether
children who grow up in former high-slavery counties do worse as adults.
For Black children born 1978–1983, the Opportunity Atlas says they do
not: compared with Black children from families at the same income level
elsewhere in the same state, they show no detectable difference in adult
income, incarceration, high school completion, or college attendance.
The estimates are close to zero, about one percentile rank per unit of
1860 slavery. Earlier work finding lower mobility in high-slavery areas
pooled all races; that pattern mostly reflects who lives there, Black
families facing a national racial gap, rather than an extra penalty
attached to the place. The racial gap tells a slightly different story.
For children born in 1978 it was a little wider in high-slavery
counties, because white children there did slightly better; by the 1992
cohort that gradient had shrunk by about two-thirds, below detection.
Even the 1978 gradient does not survive the stricter cotton control, so
it may belong to the cotton economy rather than to slavery. The one
other signal near significance is departure: Black children from
high-slavery counties are less likely to still live in their childhood
commuting zone as adults.

**Homes.** Homeownership is the surprise. In 1970 it shows no slavery
gradient. Since then, Black households in former high-slavery counties
have become *more* likely to own their homes than Black households
elsewhere in the South, and the racial gap there has become smaller.
This survives the cotton and density controls. It is unlikely to signal
prosperity, since the same counties had lower schooling and higher
poverty through 2000. More plausible explanations are that renters were
the ones who left during the migrations, that rural housing in the Black
Belt is very cheap to own, and that much Black-owned land there is
heirs' property held without clear title. Home values point to the
cheap-housing reading. In 2018–2022, in a county that was 60% enslaved
in 1860, Black-owned homes were worth about 22% less relative to
white-owned homes in the same county than in a county with no slavery,
one of the stronger modern signals in the data. It survives both cotton
controls. Higher ownership and lower relative value cancel almost
exactly: a simple housing-wealth index, ownership rate times median
value, shows no slavery gradient for Black households. The legacy shows
up not in whether Black families own, but in what their homes are worth.

<img src="../figures/static/fig06_modern_gaps_1970-2022.png"
style="width:6in;height:2.98214in"
alt="Figure 6 · NHGIS 1970–2000 census by race; ACS 5-year 2008–2012 and 2018–2022; 2010 and 2020 poverty gaps not significant" />

Figure 6 · NHGIS 1970–2000 census by race; ACS 5-year 2008–2012 and
2018–2022; 2010 and 2020 poverty gaps not significant

Taken together, these results say that a legacy can be real, large, and
long-lived in one channel while absent or even inverted in another, in
the same counties at the same time. They also show a common modern form.
In schooling, home values, and income, Black residents of former
high-slavery counties now look like Black residents elsewhere; what
remains is a wider racial gap inside those counties, driven by white
residents doing relatively better. The Opportunity Atlas finds no such
gap among children who grew up there and are measured as adults wherever
they live, which suggests the modern gap belongs to who lives in these
places now and to their local economies, perhaps shaped by who stays and
who leaves, more than to a disadvantage carried by the people raised
there.

## Two kinds of memory

The question "does the legacy of slavery still matter?" turns out to
have no single answer, because the legacy is not a single quantity. The
results resolve into at least two different kinds of memory, each with a
clear analogue in statistical physics.

**Memory held in a field, erased by flows.** The geography of Black
population is a spatial field whose overlap with the 1860 map is what β
measures, a two-time correlation function in the physicist's sense. It
separates almost cleanly into a regional amplitude times a fixed spatial
profile. For a century the dynamics acted mostly on the amplitude: a
uniform drain that shrank the pattern without reshaping it. Reshaping
requires location-specific forces, and those arrived only with return
migration into low-slavery metros. Both waves accelerated after they
began, the signature of nucleation-and-growth processes rather than the
slow, stretched relaxation typical of glasses. The memory here is not
quenched; it erodes as fast as the flows that act on it, and the flows
are currently speeding up.

**Memory quenched in cohorts, erased by turnover.** Schooling is
different. Each birth cohort's education is fixed when it passes through
school, and it carries that value for life. The adult population
therefore relaxes only through generational replacement, a renewal
process whose time constant is set by lifespans, not by any forgetting.
A sharp change in about 1970, school desegregation, appears in the adult
population as a smooth decline stretched over about fifty years. Seen
only in aggregate, it would look like slow decay; seen by cohort, it is
a step.

**Set at the quench, not by duration.** One more pattern hints at how
the memory was written. Splitting 1860 slavery into what already existed
in 1850 and what was added during the cotton boom of the 1850s, the
newer slavery predicts later outcomes at least as strongly as the older
slavery, often more; the farm ownership gap loads on the 1850s expansion
alone. Older slavery does not leave a deeper mark. What seems to matter
is the configuration at emancipation, the moment of the quench, not how
long a county had been in it. This rests on limited independent
variation, since the two shares are nearly identical in counties that
existed in both years, so it is a hint rather than a finding.

These two mechanisms answer the floor-or-zero question differently. The
population pattern has no floor in sight; whether it eventually stops
depends on whether the forces now eroding it keep running. The schooling
pattern has already stepped down to a new, lower level for every cohort
educated after desegregation, and that residual, about a third of the
old penalty, is itself still fading: the small slavery gradient in the
racial income gap shrank by about two-thirds between children born in
1978 and those born in 1992.

One more pattern runs through everything: **contingent locally,
deterministic in aggregate.** County fates scatter widely (Mitchell
frozen, Dougherty transformed, Lee whitened and then partly reversed),
yet the regional curves are smooth enough to fit with three or four
parameters. The legacy of slavery behaves less like a fixed inheritance
passed down in each place than like a macroscopic order parameter: a
well-defined average over many particular histories, each of which could
have gone differently.

## What we don't know yet

This is a draft built on a few days of analysis, and several of its
claims rest on choices that deserve more testing.

- **The frozen shape depends on how you measure it.** The century of
  near-constant relative imprint holds for raw county shares with every
  county counted equally. Measured proportionally (log shares) or
  weighted by population, the Great Migration actually sharpened the
  1860 profile until about 1970, and erosion begins then rather than
  in 1990. The broad story, a dominant slavery-shaped mode and
  accelerating erosion since 1970, holds in every version; the exact
  timing does not.

- **Correlation is not mechanism.** The design compares counties within
  states, tests against spatial noise, and controls for cotton
  suitability. It does not identify *why* a given channel persists. The
  desegregation step and the Medicare step are strong timing evidence,
  not proof of cause.

- **Neither cotton control is perfect.** The FAO suitability index fits
  the historical US cotton belt imperfectly, and actual 1860 production
  over-controls because slavery helped produce it. The truth about land
  and health lies between the two; for population, schooling and home
  values the answer is the same under both.

- **Some outcomes are thinly measured.** Early infant mortality is
  incomplete; modern county income estimates are noisy for small Black
  populations; race categories change across censuses.

- **The homeownership reversal is only partly explained.** Home values
  show the reversal is cheap ownership, not wealth, but whether the
  value gap reflects house quality, location within counties, or
  appraisal is untested. Home values for 2008–2012 would show whether
  the value gap is changing.

- **The floor is open.** The current acceleration of the population
  pattern's erosion cannot continue forever. Whether it ends in a new
  plateau or in near-complete mixing is a question for the next decades
  of data, and possibly for a mechanistic model of the migration flows
  themselves.

- **What kind of memory is this, across ages?** One contingency is one
  point on an age spectrum.

  - **Other shocks.** The project has started measuring other shocks to
    the same counties. Sherman's March (1864–65) left no detectable mark
    on population or farm values. Counties with Black Reconstruction
    officeholders still differ today, but that mostly reflects where
    freedpeople had gathered by 1870.

  - **Every decade as its own contingency.** Treating each decade's new
    piece of the population map as a contingency of known age gives a
    first age spectrum for this channel. On counties with unchanged
    boundaries since 1860, the arrangement freedpeople made in 1865–70
    has been remembered almost perfectly for 150 years. Every later
    decade's new pattern first grew for decades (momentum) and then
    decayed, at rates set by the migration regime it lived through.

  - **Reading.** Memory here is not a smooth relaxation. The
    configuration set right after emancipation is privileged, as models
    of systems quenched into a rugged landscape predict.

  - **Caveat.** This is preliminary and covers one channel.

  <!-- -->

  - **The 1927 flood** is a contrast case. Black share in flooded
    counties fell by about 4 points, as Black families left. That gap
    closed within roughly 40 years. Then it reversed: by 2000 the
    flooded counties were more Black than similar unflooded ones, while
    their population kept shrinking. A shock can be forgotten in one
    channel and come back, with the opposite sign, through another.

What the data already show clearly is that the legacy of slavery is
neither everywhere nor gone. It persists in specific channels, at
measurable strengths, with dynamics that can be read from the shape of
the curves, and in at least one case, schooling, it changed abruptly
when a barrier was finally removed.
