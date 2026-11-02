# Competitor Landscape: Instagram-like Social App with No AI-Generated Content

Research date: 2026-11-02. All facts are dated where the source allows. Network note: direct fetches of Forbes, Wikipedia, TechCrunch and socialhuman.dev failed from this session (host not in allowed domains); some pages were retrieved through the Firecrawl scraper instead, and others are cited from search-result summaries only (flagged "via search summary"). Treat search-summary items as lower-confidence than scraped pages.

### Summary table (status as of 2026-11-02 unless dated otherwise)

| App | Positioning | AI policy / enforcement | Users / traction | Funding | Fate |
|---|---|---|---|---|---|
| Cara | Artist portfolio + social, anti-AI | Bans gen-AI art; Hive automated detection + human moderation; "NoAI" tags; Glaze integration (paused for some accounts May 2024) | 40K to 650K in one week (June 2024); "over 1.5M" (Forbes, Aug 2026) | Deliberately no VC; volunteer-run PBC; GoFundMe for legal fees (Aug 2026) | Alive but under strain (scraped 3x in Aug 2026) |
| Rooverse (UK) | General "human-only walled garden" social app | Bans AI uploads; AI detection at post time + human reports; paid "RooChip Lite" credit to verify accounts | Launched April 2026; ~6 App Store ratings (very small) | Not disclosed | Early / tiny |
| SocialHuman (Helsinki) | "Real, unfiltered" social; live in-app capture only | No uploads; sensors, forensics, device attestation pipeline | Not disclosed (vendor page only) | Not disclosed | Early / unverified |
| Humanable | "AI-free" music social platform | Certifies human-only music; verified artists | Announced Aug 2025, slated Q4 2025 | Not found | Unknown whether launched |
| HumansOnly | Web social network for verified humans | Human verification; "AI agents not welcome" | Not found | Not found | Unknown / tiny |
| Cosmos | Curated image platform | "No ads, no algorithmic sludge, no AI slop" (CEO) | Not found | Not found | Alive |
| BeReal | Daily un-staged dual-camera photo | Authenticity by format (timed, front+back camera), not AI policy | Peak 73.5M users (Aug 2022); ~6M DAU by spring 2023; 23M users early 2024; Voodoo claims 40M+ "active" | $30M (2021), $85M at ~$600M valuation (2022); sold to Voodoo for ~€500M (June 2024) | Stabilized under Voodoo, ad-monetized, far below peak |
| Locket Widget | Home-screen photo widget for close friends | Format-based authenticity | 80M+ downloads, 9M+ DAU (Aug 2025); 100M+ downloads claimed later | $12.5M seed (2022, led by Sam Altman); profitable since 2024; ~$13.5M revenue | Growing / profitable |
| Retro | Private friends photo sharing (ex-Instagram) | Format-based | ~1M users (Dec 2025) | ~$21M Series A (closed Dec 31, 2025, per SEC Form D) | Growing |
| Lapse | Disposable-camera "develop later" social | Format-based | Daily installs fell ~70% from 218K peak (Oct-Nov 2023) | $30M (Feb 2024) | Social features removed Dec 2025; now camera-only (effectively dead as social) |
| Poparazzi | "Anti-selfie": friends post photos of you | Format-based | 6.2M lifetime installs; 4M MAU peak to 2-3K MAU | $2M seed (Floodgate) + $15M Series A (Benchmark) | Dead (shut June 30, 2023; capital returned) |
| Dispo | Disposable camera, photos develop next morning | Format-based | Viral invite-only in early 2021 | $4M seed (Ohanian's 776), $20M Series A (Spark, later severed) | Stalled (founder scandal 2021); still listed in store 2026 |
| Vero | Ad-free, chronological, "subscription" social | No algorithm; no AI-specific policy found | 3M downloads by March 2018 surge | Founder-funded (Ayman Hariri) | Stalled; no reliable 2025-26 user data |
| Pixelfed | Fediverse Instagram alternative | Open source, no ads; no network-wide AI ban found | ~421K network (early 2025); 904K across servers (later est.) | Grant/donation-funded | Niche, alive |
| Flashes | Photo-first Bluesky client | Inherits Bluesky moderation | 30K downloads day 1, 40.5K week 1 (Feb 2025); 100K+ later | Indie | Niche, alive |
| World ID (Tools for Humanity) | Proof-of-human identity layer for apps | Iris-scan verification badge | ~18M verified humans, ~38M World App downloads (2026) | Heavily VC-backed | Infrastructure, not a competitor app; potential partner |

## 1. Direct "anti-AI / human-made" platforms

### Takeaway
Cara is the only anti-AI visual platform with real scale (1.5M+ users by Aug 2026), but it is volunteer-run, avoided VC, and in 2026 became a target for retaliatory scraping. Every 2025-2026 general-purpose "human-only" social launch found (Rooverse, SocialHuman, Humanable, HumansOnly) is tiny or unverified; none has disclosed meaningful users or funding.

### Cited Findings
**Cara**
- Launched December 15, 2022, public testing from January 2, 2023; founded by photographer Jingna Zhang — [Wikipedia: Cara (app)](https://en.wikipedia.org/wiki/Cara_(app)) (scraped)
- Grew from about 40,000 to 650,000 users in a single week (around June 6, 2024) after Meta announced plans to train AI on user content — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app)); [Fast Company](https://www.fastcompany.com/91135674/what-is-the-cara-app); [Entrepreneur](https://www.entrepreneur.com/business-news/anti-ai-app-booming-in-popularity-as-artists-leave-instagram/475255)
- Enforcement: uses third-party AI-detection moderation from Hive — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app)); described as "a combination of automated detection and human moderation" — [The Next Web](https://thenextweb.com/news/alternative-apps-to-instagram-ai-slop-for-artists) (via search summary)
- Labels all uploads with a "NoAI" tag and works with Glaze/Nightshade — [JCK](https://www.jckonline.com/editorial-article/cara-anti-ai-platform-artists/); [ArtsHelp](https://www.artshelp.com/caras-booming-the-steady-rise-of-an-anti-ai-artist-portfolio-platform/) (via search summary)
- Glaze support added Dec 1, 2023; paused for community accounts May 29, 2024 because of abuse (multiple accounts maxing out daily Glaze credits) — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app))
- "Purposefully avoided venture funding" — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app))
- As of Aug 23, 2026: "over 1.5 million users"; described as a public benefit corporation and "a volunteer project with no financial means to respond" (Zhang quote); scraped three times in ten days; launched GoFundMe for legal defense and unforeseen server fees ("thousands of extra dollars") — [Forbes, 2026-08-23](https://www.forbes.com/sites/robsalkowitz/2026/08/23/artists-built-a-site-to-escape-ai-scrapers-are-coming-for-it-anyway/) (scraped)
- Scrapes: Aug 13, 2026 archive of ~12M works (12 TB); later 8.5M links/metadata to Hugging Face; Aug 22 a third scraper took 123K images plus bios with personal information to a torrent site. Cara is working with a volunteer on a "one-way fingerprint" called Lantern — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app)); [Forbes](https://www.forbes.com/sites/robsalkowitz/2026/08/23/artists-built-a-site-to-escape-ai-scrapers-are-coming-for-it-anyway/)
- Zhang: "I won't be bullied into making Cara members-only" — [Forbes](https://www.forbes.com/sites/robsalkowitz/2026/08/23/artists-built-a-site-to-escape-ai-scrapers-are-coming-for-it-anyway/)
- Mixed adoption: some artists joined Cara but kept Instagram after opting out of Meta's AI training — [Creative Boom](https://www.creativeboom.com/insight/everyones-talking-about-cara-but-is-it-any-good/) (via search summary)

**Rooverse (UK, Ross Thorpe)**
- UK startup set to launch platform and iOS/Android apps on April 14 (2026), banning AI-generated uploads — [Telecompaper](https://www.telecompaper.com/news/uk-startup-unveils-social-media-platform-with-protections-against-ai-content--1567677)
- Press release (April 21, 2026): launched on iOS, Android and web as a "walled garden" of human-made content — [Pressat](https://pressat.co.uk/releases/the-new-social-media-app-with-a-single-goal-a-human-only-space-with-zero-ai-content-9a4fdccea0d94fffd4abe4a67077a111/)
- Enforcement: moderation technology plus human reporting; AI detection at point of posting; new users buy a small non-withdrawable in-app credit ("RooChip Lite", explicitly not crypto) to verify, as friction against bots — [Google Play](https://play.google.com/store/apps/details?id=com.theprescientpachyderm.rooverse); [App Store](https://apps.apple.com/gb/app/rooverse/id6760191876)
- App Store listing showed only ~6 ratings (signal of very small user base); no funding disclosed; founder podcast raised the question of business viability without answering it — [App Store](https://apps.apple.com/gb/app/rooverse/id6760191876); [The Sunday Draft](https://thesundaydraft.substack.com/p/is-the-internet-still-real-with-ross)

**SocialHuman (Helsinki)**
- Free iOS/Android app; every photo/video must be captured live in the in-app camera (no uploads) and passes a verification pipeline (sensors, forensics, device attestation) — [socialhuman.dev](https://socialhuman.dev/no-ai-social-network) (vendor page, via search summary; self-reported)

**Other 2025-2026 "AI-free" launches**
- Humanable: announced Aug 2025 as "world's first AI-free social media platform" for certified human-only music, slated for Q4 2025, with verified artists — [MusicRow, 2025-08](https://musicrow.com/2025/08/humanable-to-launch-worlds-first-ai-free-social-media-platform1/)
- HumansOnly: web network requiring human verification, "AI agents not welcome" — [humansonly.wiki](https://www.humansonly.wiki/)
- Cosmos: curated image platform; CEO: "There's no ads or algorithmic sludge, no AI slop" — [Dazed](https://www.dazeddigital.com/life-culture/article/69298/1/5-social-media-platforms-actually-social-perfectly-imperfect-cosmos) (via search summary)
- Counter-trend: AI-only social apps exist (Charm, Aspect, Butterflies) and a bots-only network drew buzz in Feb 2026 — [App Store: Charm](https://apps.apple.com/us/app/charm-ai-only-social-media/id6753083338); [App Store: Aspect](https://apps.apple.com/app/id6502742786); [NPR, 2026-02-07](https://www.npr.org/2026/02/07/nx-s1-5697392-e1/a-new-social-media-platform-creates-buzz-but-its-just-for-ai-bots)

**Proof-of-humanity**
- World ID being rolled out to Zoom, Tinder and DocuSign (April 2026), with a verified-human profile badge — [Cyber Magazine](https://cybermagazine.com/news/world-id-to-verify-humans-on-zoom-tinder-and-docusign)
- ~18M verified humans across ~160 countries; ~38M World App downloads (2026 figures, secondary sources) — [Plisio](https://plisio.net/crypto/worldcoin); [Wikipedia: World](https://en.wikipedia.org/wiki/World_(blockchain)) (via search summary)
- World's own blog names gaming, dating and social networks as where proof-of-human matters most — [World.org](https://world.org/blog/announcements/at-last-trust-in-the-age-of-ai)
- Skeptic view: many verified mainly for token rewards — [WorldReview1989, 2026-09](https://www.worldreview1989.com/2026/09/worldcoin-review.html) (low-quality investment blog)

### Inferences
- Cara proves demand spikes are event-driven (Meta's AI-training news), and the core audience is professional artists protecting their work, not general consumers avoiding AI slop. A general Instagram-like app would be a different market.
- An anti-AI platform becomes a target: scraping/harassment imposes legal and infrastructure costs, which a volunteer, non-VC model struggles to absorb.
- Enforcement methods split into three approaches: (a) detect-and-remove after upload (Cara/Hive, Rooverse); (b) capture-only provenance (SocialHuman, device attestation); (c) identity verification (World ID, Rooverse's paid credit, HumansOnly). Detection alone is an arms race, so capture-provenance plus identity looks like the stronger moat.
- World ID is more likely a partner or infrastructure than a competitor; a startup could integrate it.

### Gaps
- "Not Real Art": found no reliable sources on its current state, users or funding.
- Humanity Protocol: no results on a social app built on it.
- No user or funding numbers for Rooverse, SocialHuman, Humanable, HumansOnly or Cosmos. Could not confirm Humanable ever launched.
- No Product Hunt or Hacker News data on 2025-2026 "no AI" launches was retrieved.
- Cara's revenue model and current MAU (vs. registered "users") are not public.

## 2. Authenticity-focused photo apps

### Takeaway
Format-driven "authentic" photo apps follow a boom-bust pattern: BeReal, Poparazzi, Dispo and Lapse all went viral and then lost most of their users. The survivors are close-friends utilities (Locket, profitable; Retro, $21M Series A) or the sale of BeReal to Voodoo. Open-protocol alternatives (Pixelfed, Flashes) stay niche.

### Cited Findings
**BeReal**
- Founded 2020 (Alexis Barreyat, Kévin Perreau); $30M round led by a16z and Accel (June 2021); $85M led by DST at ~$600M valuation (May 2022) — [Wikipedia: BeReal](https://en.wikipedia.org/wiki/BeReal) (scraped)
- Grew from 21.6M to 73.5M users between July and August 2022; DAU fell from 15M (Oct 2022) to about 6M (late spring 2023); 23M users at start of 2024 — [Wikipedia](https://en.wikipedia.org/wiki/BeReal)
- Acquired by Voodoo June 2024 for a reported €500M (~$537M); Voodoo claimed "more than 40 million active users" without defining daily/monthly — [Voodoo](https://voodoo.io/news/voodoo-acquires-bereal); [TechCrunch, 2024-06-15](https://techcrunch.com/2024/06/15/deal-dive-bereal-got-its-best-case-scenario-exit) (via search summary)
- 28 staff laid off shortly after acquisition (2024) — [Game Developer](https://www.gamedeveloper.com/business/bereal-lays-off-28-staffers-post-voodoo-acquisition); [Mobile Marketing Magazine](https://mobilemarketingmagazine.com/bereal-voodoo/)
- US ad platform launched April 2025, citing ~40M MAU globally and 5M US MAU — [SearchLogistics](https://www.searchlogistics.com/learn/statistics/bereal-statistics/) (secondary); contradicted by third-party trackers putting MAU nearer 16M in early 2025 — [Charle Agency](https://www.charleagency.com/articles/bereal-statistics/) (secondary)
- Revenue: ~€30M in 2025 per Voodoo (currency inconsistent across sources); third-party 2026 estimates much lower at $5-10M/yr — [Flinque](https://www.flinque.com/blog/bereal-update-everything-you-need-to-know/) (secondary; low confidence)
- During the 2026 FIFA World Cup, BeReal temporarily allowed unlimited posts instead of its once-a-day limit — [Wikipedia](https://en.wikipedia.org/wiki/BeReal)

**Locket Widget**
- 80M+ total downloads and 9M+ DAU; profitable since 2024; $13.5M annual revenue disclosed to TechCrunch (Aug 2025); revenue ~50% Locket Gold subscription, ~50% ads; $12.5M seed (2022) led by Sam Altman, no raise since — [What A Startup](https://whatastartup.substack.com/p/he-built-an-app-for-his-girlfriend-and-ended-up-having-80-million-total-downloads); [Review Rounds](https://review-rounds.com/locket-business-model-profitable-photo-widget-app/) (secondary, citing TechCrunch)
- Later profile: 100M+ downloads, ~9-10M DAU; headcount ~10 (May 2026) — [Systemaic](https://www.systemaic.com/teardowns/locket-widget) (secondary); Dealroom lists revenue under $1M, which conflicts — [Dealroom](https://dealroom.co/companies/locket/)

**Retro**
- ~1M users and new "Rewind" feature (Dec 2025); ~$21M Series A for Lone Palm Labs closed Dec 31, 2025 per SEC Form D — [TechCrunch, 2025-12-12](https://techcrunch.com/2025/12/12/retro-a-photo-sharing-app-for-friends-lets-you-time-travel-through-your-camera-roll/); [RuntimeWire](https://runtimewire.com/article/retro-ex-instagram-founders-raised-21m-private-photo-sharing) (via search summary)

**Lapse**
- Raised $30M (Feb 27, 2024) — [Wikipedia: Lapse](https://en.wikipedia.org/wiki/Lapse_(social_network)) (via search summary)
- Daily installs fell ~70% from ~218K peak (Oct 2023) to ~63K; growth relied on forced friend invites — [Appfigures](https://appfigures.com/resources/insights/20231117?f=5); [TechCrunch, 2023-11-27](https://techcrunch.com/2023/11/27/lapse-a-photo-app-that-forced-users-to-invite-friends-is-running-out-of-steam/)
- Nov 3, 2025 announcement: chose to "close down completely or simplify"; removed Feed, Profile and Chat in early Dec 2025, keeping a camera app — [Wikipedia](https://en.wikipedia.org/wiki/Lapse_(social_network)); [Threads user post](https://www.threads.com/@_mliu/post/DQnQp5NAApi/sad-that-lapse-is-removing-the-social-features-within-the-app-for-the-last); [Protect Young Eyes](https://www.protectyoungeyes.com/apps/lapse-app-review-is-it-safe). An unofficial TikTok page claims data removal on May 31, 2026 due to cost — [TikTok](https://www.tiktok.com/discover/lapse-app-shutting-down) (unverified)

**Poparazzi**
- Hit No. 1 on the App Store in 2021; ~6.2M lifetime installs (Apptopia); peak ~4M MAU fell to ~2,000-3,000 MAU; $2M seed (Floodgate) and $15M Series A (Benchmark's Sarah Tavel); team moved to a new app ("Made with Friends"); shutdown announced on Medium, users had until June 30, 2023; capital returned to investors — [TechCrunch, 2023-05-01](https://techcrunch.com/2023/05/01/once-hot-photo-sharing-social-app-poparazzi-is-shutting-down/) (scraped)
- Founders said in mid-2022 they had a two-year runway — [The Dead Pixels Society](https://thedeadpixelssociety.com/poparazzi-photo-sharing-app-shuts-down/)

**Dispo**
- Disposable-camera app; photos "develop" at 9 a.m. next day; $4M seed led by Alexis Ohanian's firm, $20M Series A led by Spark Capital; Spark severed ties in March 2021 after allegations against co-founder David Dobrik — [Wikipedia: Dispo](https://en.wikipedia.org/wiki/Dispo); [dot.LA](https://dot.la/dispo-20m-raise-2650748803.html); [CNBC, 2021-03-04](https://www.cnbc.com/2021/03/04/dispo-for-iphone-is-the-picture-sharing-app-everyones-talking-about.html) (via search summary)
- A Softonic listing shows an app update on March 24, 2026 (still listed) — [Softonic](https://dispo.en.softonic.com/iphone) (low confidence)

**Vero**
- Surged from <150K to 3M downloads by early March 2018, driven by Instagram artists; planned free access for first 1M users, then subscription — [Phonandroid](https://www.phonandroid.com/vero-deja-3-millions-de-comptes-premiers-scandales.html); [Expanded Ramblings](https://expandedramblings.com/index.php/vero-facts-statistics/) (via search summary)
- Backlash over founder Ayman Hariri's history in 2018 — [Cheddar](https://www.cheddar.com/media/the-shady-history-behind-hot-new-app-vero/)

**Open protocol alternatives**
- Pixelfed apps passed 10,000 downloads in two days (Feb 2025) — [TechCrunch, 2025-02-09](https://techcrunch.com/2025/02/09/these-apps-are-building-instagram-alternatives-on-open-protocols/); main server ~220K users, network ~421K (early 2025) — [DiverseTechGeek](https://www.diversetechgeek.com/pixelfed-2025-edition/); 904K across servers (later estimate) — [Exploding Topics](https://explodingtopics.com/blog/decentralized-social-media)
- Flashes (Bluesky photo client): ~30K downloads in first 24h, 40.5K by end of launch week (Feb 2025) — [TechCrunch, 2025-02-28](https://techcrunch.com/2025/02/28/bluesky-based-instagram-alternative-flashes-launches-publicly); passed 100K downloads (undated) — [Exploding Topics](https://explodingtopics.com/blog/decentralized-social-media); launch coverage — [PetaPixel, 2025-02-25](https://petapixel.com/2025/02/25/bluesky-photo-app-flashes-launches-on-the-app-store/)

### Inferences
- The survivors (Locket, Retro, BeReal at reduced scale) serve small, real-friend graphs, not public discovery feeds. This suggests "authenticity" sustains as a close-friends utility more than as an Instagram-scale public network.
- Locket's profitability with ~10 staff shows a lean model works; BeReal's ~$600M valuation to ~€500M exit came only after users fell sharply from the peak.

### Gaps
- Glass (paid photography app): no search results; current subscribers/status unknown.
- Foto, Grain and generic "Unfiltered/no-filter" apps: not researched successfully; no data found.
- No 2025-2026 user figures for Vero, Dispo, Pixelfed or Flashes. Vero's leadership status in 2026 is unconfirmed (only a low-quality source).
- BeReal's true 2026 MAU is disputed (16M vs 40M); Voodoo does not define "active."

## 3. Lessons from failed authenticity apps (retention and network effects)

### Takeaway
Viral launch mechanics (invite gates, forced invites, novelty formats, celebrity founders) produce download spikes but not retained networks. Poparazzi lost ~99.9% of MAU, BeReal lost ~60% of DAU within months, and Lapse's installs fell 70% within weeks. A "no AI" pitch risks the same pattern if it is a novelty rather than a daily habit with a friend graph.

### Cited Findings
- Poparazzi: peak ~4M MAU to ~2-3K MAU despite $17M raised and a No. 1 ranking; founders pivoted and returned capital — [TechCrunch, 2023-05-01](https://techcrunch.com/2023/05/01/once-hot-photo-sharing-social-app-poparazzi-is-shutting-down/)
- Poparazzi founders' stated philosophy: most social apps fail, so keep building and experimenting until one hits — [TechCrunch](https://techcrunch.com/?p=2328335) (via search summary)
- BeReal DAU 15M (Oct 2022) to ~6M (spring 2023) — [Wikipedia](https://en.wikipedia.org/wiki/BeReal)
- Lapse: growth relied on making users invite friends; installs fell ~70% within weeks once the mechanic was relaxed — [TechCrunch, 2023-11-27](https://techcrunch.com/2023/11/27/lapse-a-photo-app-that-forced-users-to-invite-friends-is-running-out-of-steam/); [Appfigures](https://appfigures.com/resources/insights/20231117?f=5). By Nov 2025 it removed social features because running at scale was unsustainable — [Wikipedia](https://en.wikipedia.org/wiki/Lapse_(social_network))
- Product Hunt discussion framed Lapse as "a cautionary tale for social products that prioritize disposable sharing" — [Product Hunt](https://www.producthunt.com/p/lapse-3/lapse-a-cautionary-tale-for-social-products-that-prioritize-disposable-sharing)
- Dispo lost its lead investor within weeks of going viral because of founder controversy — [Wikipedia: Dispo](https://en.wikipedia.org/wiki/Dispo)
- Vero spiked in 2018 on artist migration from Instagram (the same trigger as Cara in 2024) and faded — [Phonandroid](https://www.phonandroid.com/vero-deja-3-millions-de-comptes-premiers-scandales.html)

### Inferences
- Instagram-exodus spikes (Vero 2018, Cara 2024) are triggered by incumbent policy outrage, and they fade unless the new app gives a reason to return daily. Migration needs a creator's audience to follow, which rarely happens.
- A "no AI" positioning is a values claim, like "no algorithm" (Vero) or "no filters" (BeReal). Values alone have not retained users; utility for real friends (Locket) has.
- Lapse shows a cost trap: authenticity apps with heavy media hosting and weak monetization are expensive at scale. Cara's server-fee strain in 2026 fits the same pattern.

### Gaps
- No public cohort retention curves (D1/D30) for any of these apps were found; the evidence is MAU/DAU snapshots and install estimates.

## 4. How incumbents handle AI content (and whether they undercut a startup)

### Takeaway
As of Nov 2026, TikTok (Nov 2025) and Pinterest offer "see less AI" controls, but neither fully removes AI content. Instagram and YouTube rely on labels and offer no viewer-side "hide AI" switch. Instagram's leadership has publicly conceded detection will fail and is pivoting to verifying real media and people. Incumbents have partly undercut "less AI" but not "zero AI, guaranteed," which leaves a narrow opening.

### Cited Findings
**TikTok**
- Nov 21, 2025: added a control in Settings > Content Preferences > Manage Topics to see more or less AI-generated content in For You; it adjusts mix "rather than removing or replacing content in feeds entirely"; adding invisible watermarks to content made with TikTok AI tools (e.g., AI Editor Pro) and reading C2PA Content Credentials; launched a $2M AI Literacy Fund — [Digital Music News, 2025-11-21](https://www.digitalmusicnews.com/2025/11/21/tiktok-ai-toggle-how-to-use/) (scraped); [eMarketer](https://www.emarketer.com/content/genai-content-increases-tiktok-adds-filter-ai-weary-users)
- Slider affects only For You; AI clips still appear in Search/Following; relies on labels so unlabeled AI slips through — [Make Tech Easier](https://maketecheasier.com/reduce-ai-content-tiktok/) (via search summary)

**Pinterest**
- "Refine your recommendations" includes an AI content section to see fewer GenAI Pins in certain categories; each AI Pin has a "See fewer AI Pins" option; filtering depends on metadata, classifiers or creator disclosure, so undetected AI still appears — [Pinterest Help](https://help.pinterest.com/en/article/tune-your-home-feed); [Metricool](https://metricool.com/pinterest-ai/); [ThatPainter](https://thatpainter.com/pinterests-tuner-can-reduce-ai-content-in-your-feed-but-not-remove-it-entirely/) (via search summary)

**Instagram / Meta**
- Meta began labeling AI-generated images on Instagram/Facebook (announced Feb 2024) — [NPR, 2024-02-06](https://www.npr.org/2024/02/06/1229317971/meta-labeling-ai-generated-images-instagram-facebook-artificial-intelligence)
- Adam Mosseri (Jan 2026 coverage) argued platforms will get worse at detecting AI over time and that it may be more practical to fingerprint real media, suggesting camera makers sign images at capture; Instagram is shifting focus to verifying who shared something — [TechRadar](https://www.techradar.com/ai-platforms-assistants/ai-slop-won-in-2025-fingerprinting-real-content-might-be-the-answer-in-2026); [Tom's Guide](https://www.tomsguide.com/ai/instagram-says-ai-killed-the-curated-feed-now-its-scrambling-to-prove-whats-real); [Creative Bloq](https://www.creativebloq.com/art/digital-art/instagrams-boss-admits-ai-slop-has-won-but-where-does-that-leave-creatives)
- May 6, 2026: Instagram added an optional "AI creator" account label; it does not affect recommendation distribution — [MediaPost, 2026-05-06](https://www.mediapost.com/publications/article/414862/instagram-unveils-new-ai-creator-account-label.html)
- No master switch to hide AI content on Instagram as of 2026; workaround is muting keywords like "AI-generated" — [Oreate AI](https://discover.oreateai.com/discover/why-you-cant-fully-block-ai-on-instagram-and-what-to-do-instead); [Inro](https://www.inro.social/blog/meta-ai-instagram-guide) (third-party; via search summary)
- July 2026: Meta removed its "Muse Image" feature that let people generate AI images referencing public Instagram accounts, after criticism; a reuse toggle governs letting others create with your content — [Malwarebytes, 2026-07](https://www.malwarebytes.com/blog/ai/2026/07/turn-off-this-meta-setting-before-someone-generates-ai-images-of-you); [TechCrunch, 2026-07-09](https://techcrunch.com/2026/07/09/how-to-stop-metas-ai-image-generator-from-using-your-instagram-photos/)
- Unverified claim: Instagram renamed a label "AI-generated profile" on Aug 31, 2026 — [removeailabel.com](https://removeailabel.com/blog/how-to-turn-off-ai-info-on-instagram) (low-quality source)

**YouTube**
- Creators must disclose realistic altered/synthetic content; May 2026 update made a single, more prominent label for photorealistic AI content, aligned with EU AI Act wording; YouTube says it is reducing low-quality AI "slop" via spam systems and monetization rules; no viewer-side filter to hide AI videos — [MiniMatters, 2026-05](https://minimatters.com/youtube-ai-content-labeling-update-in-may-2026/); [Android Central](https://www.androidcentral.com/apps-software/youtube/youtube-will-help-creators-use-ai-in-2026-as-long-as-its-not-slop); [Oreate AI](https://discover.oreateai.com/discover/how-to-effectively-filter-out-aigenerated-content-and-reclaim-your-youtube-feed) (mostly secondary)

### Inferences
- The incumbents' "see less AI" controls reduce the "I just want fewer AI posts" pitch, but their reliance on labels and detection means they cannot promise zero AI. A startup's differentiator would be a guarantee (capture-only plus provenance plus identity), not a filter.
- Mosseri's "fingerprint real content" stance signals Instagram may itself move toward provenance (C2PA, verified capture). If Meta ships a "verified real" badge or filter, it would directly undercut the core startup value proposition. This is a key risk to monitor.

### Gaps
- Exact launch date of Pinterest's "see fewer AI Pins" control was not confirmed from a primary source in this session.
- No evidence found that Instagram or YouTube shipped a viewer-side "hide AI" toggle as of Nov 2026.
- No data on how many users actually use TikTok's or Pinterest's AI controls.

## 5. Acquisitions, funding rounds and market sizing

### Takeaway
Capital has flowed to "authentic" friend-photo apps (BeReal €500M exit, Retro $21M, Lapse $30M, Locket $12.5M), not to explicitly anti-AI platforms. Cara refused VC, and no 2025-2026 "AI-free" startup with disclosed funding was found. No credible market-size estimate for "AI-free social" exists.

### Cited Findings
- BeReal acquired by Voodoo, June 2024, ~€500M (~$537M) — [Voodoo](https://voodoo.io/news/voodoo-acquires-bereal); [Wikipedia](https://en.wikipedia.org/wiki/BeReal); analysis of the deal — [Naavik](https://naavik.co/digest/is-voodoo-deal-just-optimistic/); [Konvoy](https://www.konvoy.vc/newsletters/voodoo-gets-real)
- Retro ~$21M Series A (Dec 31, 2025) — [TechCrunch](https://techcrunch.com/2025/12/12/retro-a-photo-sharing-app-for-friends-lets-you-time-travel-through-your-camera-roll/); [RuntimeWire](https://runtimewire.com/article/retro-ex-instagram-founders-raised-21m-private-photo-sharing)
- Lapse $30M (Feb 2024), then removed social features (Dec 2025) — [Wikipedia: Lapse](https://en.wikipedia.org/wiki/Lapse_(social_network))
- Locket $12.5M seed (2022), profitable since 2024 — [Review Rounds](https://review-rounds.com/locket-business-model-profitable-photo-widget-app/)
- Poparazzi $17M total, shut down, capital returned (2023) — [TechCrunch](https://techcrunch.com/2023/05/01/once-hot-photo-sharing-social-app-poparazzi-is-shutting-down/)
- Dispo $24M total (2021) — [dot.LA](https://dot.la/dispo-20m-raise-2650748803.html)
- Cara: no VC; GoFundMe for legal fees (Aug 2026) — [Wikipedia](https://en.wikipedia.org/wiki/Cara_(app)); [Forbes](https://www.forbes.com/sites/robsalkowitz/2026/08/23/artists-built-a-site-to-escape-ai-scrapers-are-coming-for-it-anyway/)
- Rooverse, SocialHuman, Humanable: no funding disclosed — [Pressat](https://pressat.co.uk/releases/the-new-social-media-app-with-a-single-goal-a-human-only-space-with-zero-ai-content-9a4fdccea0d94fffd4abe4a67077a111/); [MusicRow](https://musicrow.com/2025/08/humanable-to-launch-worlds-first-ai-free-social-media-platform1/)

### Inferences
- Investors fund "authentic social" when it comes with a viral friend-graph mechanic and a strong team (ex-Instagram for Retro). "No AI" as the main thesis has no VC-backed comparable yet, which means either white space or a sign investors see it as a feature rather than a company.
- Possible exits: acquisition by a scaled app group (Voodoo-style) or an incumbent wanting provenance tech, more than a standalone IPO-scale network.

### Gaps
- No market sizing (TAM/SAM) for "AI-free" or "human-verified" social found; no Sensor Tower/Appfigures category reports on this niche.
- No Crunchbase data retrieved directly (fetches restricted); funding figures come from press and Form D reports.
