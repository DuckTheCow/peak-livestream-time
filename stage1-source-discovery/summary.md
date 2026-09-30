# Stage 1-2 summary: source coverage

Each cell gives the best tier found. **p** means proxy only (no direct measure of the indicator), and **pending** means the tier awaits the owner's decision (see tier_questions.md). For I5, the cell also says whether the published tables give a time-of-day profile (**ToD**).

| Region | I1 live-stream viewing | I2 English ability | I3 English x viewing | I4 content language | I5 time of day | I6 media at work/study |
|---|---|---|---|---|---|---|
| United States | 2 p (NTIA online video by age) | 2 (ACS; 5-17/18-64/65+) | gap | 2 p (Pew, Hispanic adults' news language) | 1 ToD (ATUS A-3 hourly, all days and ages pooled) | gap (ATUS has no secondary media activity) |
| United Kingdom | pending (Ofcom AMLT live-stream by age); 2 p (Eurostat 2018) | 2 (E&W and NI censuses; Scotland gap) | gap | gap | 1, daily totals only (OTUS) | 1 p (main-activity audio only) |
| Canada | 2 (CIUS 2022 live-streaming item; 15-24 and total only) | 2 (Census 2021 by age) | gap | gap | 1 ToD (5-min, weekday/weekend, 4 age bands) | 1 p (leisure simultaneous with paid work) |
| Australia | 2 p (ACMA video/YouTube/Twitch) | 2 (Census 2021; age split needs TableBuilder) | gap | gap | 1 ToD for paid work only (2024); full ToD only in COVID-era 2020-21 | 1 p (2020-21 secondary audio) |
| Ireland | 2 p (Eurostat 2024 video) | 2 (Census 2022, non-native speakers only, no age) | gap | pending p (EB540) | pending, daily totals only (ESRI 2005) | pending p |
| New Zealand | 2 p (Stats NZ 2012, superseded); pending p (NZ On Air) | 2 (Census 2023 totals; age tables need API key) | gap | gap | gap (2009-10 tables not accessible) | gap |
| Mexico | 2 p (ENDUTIH 2025) | gap | gap | gap | pending, weekly totals only (ENUT not a diary) | gap |
| Mainland Europe (29) | 2 p (Eurostat 2024 video; IS 2020; CH BFS) | 2 p (AES, not English-specific); pending (EB540 English by country) | gap | pending p (EB540; not NO/CH/IS) | 1 ToD pooled days, sex only (10 countries 2020 round, 10 older waves; 9 gap) | 1 p (daily totals) |
| India | 2 p (internet use) | 2 (Census 2011 counts, no age) | gap | gap | 1, daily totals only (TUS 2024, 30-min diary) | 1 p |
| Philippines | 2 p (DHS women 15-49) | gap (not accessible) | gap | gap | gap | gap |
| Nigeria | 2 p (DHS internet use) | gap | gap | gap | 1, daily totals only (4 states) | 1 p |
| South Africa | 2 p (household access only) | 2 (home language only) | gap | gap | 1, daily totals only (2010, Q4 only) | 1 p (2010) |
| Singapore | 2 p (IMDA internet use) | 2 (literacy, home language) | gap | gap | gap | gap |

## Caveats that most affect the model

1. **No direct live-stream measure outside Canada.** The only Tier 1 or 2 direct live-stream item is the Canadian Internet Use Survey 2022, published for ages 15-24 and total only. The UK Ofcom item is tier pending, and every other region relies on online-video or internet-use proxies with differing wording.
2. **I3 is missing everywhere.** No published table crosses English ability with video or live-stream use, and no microdata file found holds both variables. The joint distribution will have to be assumed.
3. **Weekday/weekend time-of-day profiles are published only for Canada.** Even there, about half the age-band cells are suppressed (".."). The US table pools all days and ages, HETUS pools days and splits by sex only, and the UK, Ireland, Mexico, India, Nigeria and South Africa publish daily totals only. Half-hour profiles will need microdata: ATUS (open), Canada PUMF, India TUS 2024 (registration), UKTUS 2014-15 (registration), OTUS (secure).
4. **Partial-year collection.** ATUS 2025 has no data for 1 Oct to 12 Nov 2025. ABS 2024 ran only Jul to Oct 2024, ENUT only Oct to Nov 2024, South Africa 2010 only in Q4, and OTUS in discrete waves.
5. **COVID-era fieldwork.** Affected sources are ABS 2020-21 (Australia's only full time-of-day tables), HETUS for EE, FI, AT and NL, CIUS 2020, Sweden TID 2021 and the OTUS 2020-21 waves.
6. **Old editions.** The latest diary is 2010 for South Africa, 2009-10 for New Zealand and 2005 for Ireland. Ten EU countries have only HETUS 2000 or 2010 waves. India's language data are from the 2011 census.
7. **English ability measures are not comparable.** They differ in scale (4-point in the US, UK, Australia and Ireland; "can conduct a conversation" in Canada, NZ and EB540; literacy in Singapore; home language in South Africa) and in who is asked (Australia and Ireland ask only non-English home-language speakers). No official English-specific table exists for mainland Europe, and EB540 has age only at EU27 level.
8. **Denominators vary.** Figures are shares of all persons, of internet users (Eurostat PC_IND vs PC_IND_IU3) or of activity participants (ABS 2024 Table 14 is the share of that day's paid-work participants, not of the population). This must be resolved before any combination.
9. **Secondary activity is largely unavailable.** ATUS does not collect it, ABS dropped it in 2024, OTUS collects it but does not publish it, and HETUS gives daily totals only. I6 therefore rests on proxies.
10. **Some figures were read indirectly.** Ofcom, the Philippines (PSA/DICT), NSO Malta, ITU DataHub, Stats NZ Data Explorer and ABS TableBuilder were blocked or needed credentials. BLS and Ofcom figures were read through summarising fetch tools and should be checked against the source files in stage 3.
