# Technical Feasibility of Enforcing "Absolutely No AI-Generated Content" on an Instagram-like App

Research date: 2026-11-02. Source-quality note: several of the most detailed 2026 status sources (lumethic.com, c2paviewer.com) are vendor/explainer sites with a commercial interest in provenance verification; their claims are flagged where used. Several findings come from search-result excerpts rather than full-page reads and are marked "(excerpt)".

## 1. C2PA / Content Credentials: adoption status (2026), survival through uploads, platform use, limitations

### Takeaway
C2PA capture-signing exists on a small set of devices (Pixel 10/11 by default, roughly 17 pro cameras from Leica/Sony/Canon/Nikon, often opt-in or licensed), but not on iPhones (Apple shipped its own non-C2PA "Reference Image" on iPhone 18 Pro in Sept 2026) and not on unedited Samsung photos. Most major platforms strip C2PA on upload. So C2PA can serve as a positive "verified human capture" signal for a minority of uploads. It cannot serve as a universal gate.

### Cited Findings
**Phones**
- Google Pixel 10 (announced Made by Google, Aug 2025) adds C2PA Content Credentials in Pixel Camera and Google Photos. Pixel Camera achieved C2PA Conformance Program **Assurance Level 2**, "the highest security rating currently defined" — [Google blog](https://blog.google/security/pixel-android-trusted-images-c2pa-content-credentials/) (excerpt)
- Pixel 10 keys are generated/stored in the Titan M2 chip, and Tensor G5 does the cryptography. Every Pixel Camera photo is signed by default with no setting. Offline on-device timestamping is supported. Google Photos records edits, AI or otherwise, in updated credentials — [Lumethic, "Which Phones Sign Photos with Content Credentials in 2026" (updated 2026-09-16; vendor source)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- Pixel 11 (announced Aug 12, 2026) continues default signing on a new Titan M3 chip. Re-certification is not yet published. At I/O in May 2026, Google announced video-capture signing and a backport to Pixel 8/9, with the scope of the photo backport unconfirmed — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- Critics: Hacker Factor's blog (Sept 5, 2025) titled its analysis "Google Pixel 10 and Massive C2PA Failures" and noted Pixel Camera was then the *only* AL2 product on the conforming list — [Hacker Factor](https://hackerfactor.com/blog/index.php?/archives/1077-Google-Pixel-10-and-Massive-C2PA-Failures.html) (excerpt). A Privacy Guides forum post says Google reuses the same root certificates across the Pixel 10 lineup, so a signature cannot attest to a specific device — [Privacy Guides forum](https://discuss.privacyguides.net/t/missing-warnings-about-the-c2pa/36436) (excerpt; community source)
- Samsung Galaxy S25 (Jan 2025) was the first Android phone with Content Credentials, but only on images **edited with Galaxy AI**. Unedited camera photos get nothing. The implementation is software-level without a hardware root of trust, and Samsung's certs were initially not on the C2PA trust list. The S26 (early 2026) has the same shape. Claims that the S26 signs at capture are unconfirmed — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials); corroborating: [Android Authority](https://www.androidauthority.com/galaxy-s25-content-credentials-3523256/), [TechRadar](https://www.techradar.com/phones/samsung-galaxy-phones/samsung-galaxy-s25-phones-get-content-credentials-support-and-i-couldnt-be-happier-for-creators) (excerpts)
- Vivo X300 Pro reportedly attaches Content Credentials at capture since Oct 2025. Lumethic says it has not verified this. Sony Xperia phones ship none — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- **iPhone:** no iPhone supports C2PA. On Sept 9, 2026, Apple launched **Apple Reference Image** on the iPhone 18 Pro/Pro Max. It is opt-in and saves a second "reference" copy with a unique ID in metadata. Capture telemetry (hardware IDs, sensor signatures) goes to Apple Private Cloud Compute, which creates a signature tying the image to that iPhone. Apple calls it a "digital negative." Apple has not joined Content Credentials — [Nieman Lab, Sept 9, 2026](https://www.niemanlab.org/2026/09/apple-launches-a-new-way-to-prove-a-photo-was-shot-with-an-iphone-not-generated-by-ai/)
- Apple Reference Image covers only the Main camera on two models. It has no published file format and no verifier outside Apple's apps, no C2PA validator can read it, and capture is switched off in the EU at launch — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials); PetaPixel (Oct 12, 2026) similarly notes you must "buy an iPhone 18 Pro, only use the main camera…" — [PetaPixel](https://petapixel.com/2026/10/12/apple-content-authenticity-and-the-war-to-prove-whats-real/) (excerpt)

**Dedicated cameras** (per [Lumethic camera list, updated 2026-09-16; vendor source](https://www.lumethic.com/en/articles/cameras-with-c2pa-content-credentials)): about 17 cameras sign at capture. Fujifilm and Panasonic do not yet.
- Leica: M11-P (late 2023), M11-D (2024, must be activated), SL3-S (Jan 2025, must be activated)
- Sony: Alpha 1, 1 II, 7 IV, 7 V (Dec 2025), 7R V, 7R VI (June 2026), 7S III, 9 III, FX3, FX30, PXW-Z300. All require Sony's **licensed** Camera Authenticity Solution, i.e. aimed at enterprise/news.
- Canon: EOS R1 and R5 Mark II via firmware (July 2025)
- Nikon: Z6III got C2PA in firmware 2.00 (Aug 27, 2025). A flaw in multiple-exposure mode let users sign a manipulated image, so Nikon **suspended its Authenticity Service and invalidated all issued certificates** starting Sept 2025.

**Survival through uploads / platform use**
- Social platforms re-encode almost every upload. The typical pipeline reads C2PA at upload to inform a label, then discards it. Per the table: Instagram/Facebook/Threads strip C2PA from served files, read it at upload, and show an "AI info" label on AI-flagged content. TikTok historically stripped it, auto-labels "AI-generated" from C2PA markers, and has announced re-attaching credentials. LinkedIn is the only one displaying inbound credentials (CR icon with provenance panel) — [Lumethic, platforms article (vendor)](https://www.lumethic.com/en/articles/content-credentials-social-media-platforms) (excerpt)
- WhatsApp preserves credentials only when an image is sent as a document — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- Meta's "AI info" label dates from Feb 2024. Since Sept 2024 the label for AI-*edited* (vs. generated) content sits less prominently in the post menu — [Lumethic (vendor)](https://www.lumethic.com/en/articles/content-credentials-social-media-platforms) (excerpt)

**Stripping / spoofing**
- Free browser tools exist specifically to strip C2PA "to avoid Made with AI labels" — [MetaStrip](https://metastrip.app/blog/remove-c2pa-content-credentials-from-image); an iOS app (PrivyClean) advertises removing C2PA to avoid Instagram/Facebook auto-labeling — [Reddit r/iosapps](https://www.reddit.com/r/iosapps/comments/1safpx6/i_added_ai_metadata_detection_to_privyclean_it/) (excerpts)
- Nikon Z6III incident (above): a signed-but-manipulated image shows that a signing implementation itself can be defeated — [Lumethic (vendor)](https://www.lumethic.com/en/articles/cameras-with-c2pa-content-credentials)

### Inferences
- Stripping is trivial, so a *missing* C2PA manifest proves nothing. C2PA only works as an allow-list signal ("valid capture manifest from a trusted device, no AI-edit actions"), never as a deny signal.
- If the app *required* valid capture-time C2PA, it could today accept only Pixel 10/11 users, a few Vivo users, and pro-camera owners. That excludes every iPhone user (most of the US market) and all unedited Samsung photos. That is not viable as a mass-market gate in 2026.
- Apple's proprietary approach fragments the ecosystem. Supporting iPhones would require integrating Apple's verifier, if Apple exposes one (it does not appear to be public). EU users would be excluded even on iPhone 18 Pro.
- The app must build its own pipeline to read and verify manifests *before* re-encoding, and should consider re-attaching or displaying credentials as LinkedIn does.

### Gaps
- No primary data found on the share of uploads on any platform that carry valid C2PA.
- Couldn't confirm TikTok's re-attachment rollout status or LinkedIn's exact verification logic from primary sources.
- Did not fetch c2pa.org's conformance list directly. Number of AL2-certified products as of Nov 2026 is unknown.
- Whether Apple will offer a third-party verification API for Reference Image is unknown.

## 2. In-app camera-only capture (BeReal-style, Truepic, App Attest / Play Integrity, secure-enclave signing)

### Takeaway
Forcing capture through the app's own camera, with device and app attestation plus per-capture signing, is the strongest *generally available* enforcement option because it works on all phones, iPhones included. Its limits: an app cannot reach the hardware sensor root of trust that Pixel uses, attestation can be bypassed on compromised devices, and "re-photographing a screen" showing AI content remains a fundamental gap. It also kills uploads from pro cameras and the camera roll, which hurts creators.

### Cited Findings
- Truepic sells an SDK ("Lens") that lets any mobile app integrate its secure camera technology directly — [Truepic blog](https://www.truepic.com/blog/truepics-new-sdk-will-power-trusted-photo-capture-across-the-internet) (excerpt). Truepic now positions itself around authenticating inspection photos/videos at capture for businesses — [Truepic](https://www.truepic.com/) (excerpt). Truepic's secure camera was integrated with Microsoft's Content Integrity tools — [Truepic blog](https://www.truepic.com/blog/truepics-secure-camera-enhances-microsofts-content-integrity-tools) (excerpt)
- Third-party iOS capture apps can implement C2PA signing themselves (e.g., Lumethic Capture). However, "an app cannot reach the hardware root of trust that Pixel's implementation uses, a constraint that applies to every iOS capture app equally until Apple opens the pipeline" — [Lumethic (vendor; sells such an app)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- Guardsquare describes attacks that "can fully compromise the Play Integrity attestation service, allowing the attacker to alter app logic, tamper with memory," etc. — [Guardsquare](https://www.guardsquare.com/blog/android-and-ios-app-attestation) (excerpt)
- Play Integrity can surface signals such as missing security updates, active overlay or screen-capture apps, disabled Play Protect, and anomalous request patterns. Its predecessor SafetyNet was vulnerable to bypasses — [ODU AttestLens paper, Apr 2026 (PDF)](https://vsgc.odu.edu/wp-content/uploads/2026/04/MacDonald_Collin_Paper.pdf) (excerpt)

### Inferences
- Pros: works cross-platform today; vendor SDK (Truepic) or in-house (App Attest + Play Integrity + hardware-backed keystore signing of the capture hash at shutter time); low per-item cost compared with detectors; produces a clear, explainable rule ("captured in-app").
- Cons / attack surface: (a) **analog hole**: pointing the attested camera at a high-quality monitor showing AI imagery. This needs recapture/moiré/depth-based liveness heuristics, which are themselves probabilistic. (b) Rooted/jailbroken devices and virtual-camera injection on Android. (c) Users cannot post from DSLRs or import edited work, which alienates photographers and artists, likely a core audience for a "no-AI" app. (d) BeReal-style constraints (instant capture, no edits) also bar legitimate non-AI edits.
- A hybrid is plausible: an "attested capture" badge tier, plus a lower-trust tier for imports with valid C2PA from trusted cameras/Pixel, plus detector-screened imports.

### Gaps
- Didn't find Truepic Lens SDK pricing or BeReal's technical anti-cheat details.
- No published measurements found on the success rate of screen-recapture attacks against attested capture apps.
- Apple App Attest–specific bypass research not retrieved.

## 3. AI image/video detectors: accuracy, false positives, robustness, cost

### Takeaway
Commercial detectors range from good to poor in independent tests and frequently disagree. False positive rates on real photos ran 0–40% across tools in a May 2026 NewsGuard test. Academic in-the-wild benchmarks show 45–50% AUC drops versus lab benchmarks. Detectors also treat "lightly AI-edited" inconsistently. At roughly $1–3 per 1,000 images, cost is not the constraint. Accuracy and false accusations are.

### Cited Findings
- **NewsGuard (May 8, 2026)** tested Hive, AI or Not, ZeroGPT, Sightengine and ScamAI on 45 images (15 authentic, 15 lightly edited, 15 heavily edited) — [NewsGuard](https://www.newsguardtech.com/special-reports/leading-ai-image-detection-tools-mislead-online-users-often-declaring-authentic-content-fake/):
  - False positives on authentic photos: ScamAI 40% (6/15), ZeroGPT 20%, AI or Not 6.67%, Hive 0%, Sightengine 0%. Collectively 13.33%.
  - Heavily manipulated images caught: AI or Not 100%, ZeroGPT 93.33%, ScamAI 80%, Hive 73.33%, Sightengine 33%.
  - Lightly touched-up images flagged as AI: ScamAI 93%, AI or Not 87%, ZeroGPT 80%, Hive 27%, Sightengine 27%.
  - At least one tool disagreed on 35 of 45 images. "There is no industry consensus on what counts as AI-generated content," and tools don't state what level of manipulation triggers an AI classification.
  - Caveat: tiny sample (n=15 per class).
- **Deepfake-Eval-2024 (arXiv 2503.02857)**: on in-the-wild deepfakes circulated in 2024, open-source SOTA detectors' AUC dropped by **50% for video, 48% for audio, 45% for image** compared with prior benchmarks. One model (FGI) scored AUC 0.42 vs 0.845–0.98 on its original test sets. The dataset has 44 h video, 56.5 h audio, 1,975 images — [arXiv](https://arxiv.org/abs/2503.02857); [GitHub](https://github.com/nuriachandra/deepfake-eval-2024) (excerpts)
- A July 2026 arXiv paper (2607.13234) reports that on Deepfake-Eval-2024 the **best commercial detector scored AUC ~0.90 on images and ~0.79 on video**, vs best open-source 0.56 (image) and 0.63 (video). The authors' continuously updated system scored 0.915/0.822 — [arXiv 2607.13234](https://arxiv.org/abs/2607.13234) (excerpt; authors' own system, not independently verified)
- Hive claims "an independent study shows that Hive's AI-Generated Image and Video Detection API outperforms its competitors and human experts" in classifying human vs. AI art — [Hive](https://hivemoderation.com/ai-generated-content-detection) (vendor claim, excerpt)
- A 2026 comparison reports Sightengine "struggled with certain Nano Banana outputs" — [EmailAnalytics](https://emailanalytics.com/ai-image-detector-tools) (excerpt; low-authority source)
- Artists report Hive giving their human artwork "96% AI" — [Reddit](https://www.reddit.com/r/ChatGPT/comments/1tw2xvg/i_tested_50_realistic_chatgpt_images_on_truthscan/) (excerpt; anecdotal)

**Cost**
- Sightengine: free 2,000 ops/month; Starter $29 for 10,000; Growth $99 for 40,000; Pro $399 for 200,000 — [Eden AI, 2026](https://www.edenai.co/post/content-moderation-apis-text-image-and-video-compared) (excerpt); overage ~$0.002/operation (~$2/1K) — [Paxmod](https://www.paxmod.com/blog/content-moderation-api-pricing-comparison) (excerpt). Video is billed per sampled frame — [Eden AI](https://www.edenai.co/post/content-moderation-apis-text-image-and-video-compared)
- Hive: ~$3 per 1,000 images (third-party estimate) — [Paxmod](https://www.paxmod.com/blog/content-moderation-api-pricing-comparison) (excerpt)
- Dedicated AI-image detection APIs: ~$0.001–$0.005 per scan depending on volume — [aiimagedetectorapi.com](https://aiimagedetectorapi.com/blog/sightengine-vs-hive-vs-ai-image-detector-api/) (excerpt; competitor-written)

### Inferences
- Rough cost: at 1M uploads/day and ~$2/1K, detection costs ~$2K/day (~$730K/yr) for images, with video multiplied by frames sampled. That is meaningful for a startup but not prohibitive.
- Assume a production FPR of even 1% (better than most tools above). At 1M real uploads/day that means ~10,000 wrongly flagged human posts per day, each needing human review or causing a false accusation. Under a zero-tolerance "absolutely no AI" policy, this is the binding constraint.
- Detectors trained on older generators degrade on new ones (the in-the-wild AUC drops). Expect a recurring cat-and-mouse cycle after each major model release (Veo 3, Sora 2, Nano Banana, Midjourney v7, Flux).
- Detectors should be used only as triage for human review, never as an auto-ban.

### Gaps
- No independent 2025–2026 accuracy figures found for **Reality Defender, Illuminarty, TrueMedia, or Google's SynthID Detector** specifically. I could not confirm TrueMedia's current operating status from a source in this session.
- No rigorous per-generator benchmark (Veo 3, Sora 2, Nano Banana, Midjourney v7, Flux) from a neutral party was retrieved.
- Reality Defender and Hive enterprise pricing not published/retrieved.
- NIST GenAI evaluation results not retrieved.

## 4. Watermarking: SynthID, Meta Video Seal, OpenAI C2PA on Sora/DALL-E

### Takeaway
Watermarks only cover cooperating vendors' outputs, so open-source models (e.g., Flux run locally) carry none. Metadata-based marks (C2PA on Sora/DALL-E) are trivially stripped. Visible Sora watermarks were removed by readily available sites within days of the Sora 2 launch. Pixel-level marks like SynthID are more robust but have a growing removal-tool ecosystem, and detection is largely internal to Google. Watermarks are a helpful positive "this is AI" signal. They cannot prove the absence of AI.

### Cited Findings
- The Verge (Oct 27, 2025), "Sora is showing us how broken deepfake detection is": OpenAI's video generator embeds C2PA metadata, "but the system clearly isn't working" — [The Verge](https://www.theverge.com/report/806359/openai-sora-deepfake-detection-c2pa-content-credentials) (subheading/summary only; full text not retrievable)
- Sora 2 output carries a visible cloud-logo watermark. 404 Media reported in Oct 2025 that it tested three removal sites — [Neural Defend](https://www.neuraldefend.com/insights/topics/detecting-sora-videos) (excerpt). Observers noted "the surge in watermark removers within days of Sora 2's release" — [LinkedIn post, Jon Ippolito](https://www.linkedin.com/posts/jonippolito_sora-aiethics-aivideo-activity-7382033005072130048-T07a) (excerpt; opinion)
- Reddit users testing Sora 2 C2PA claimed OpenAI's watermark claims did not hold up in their tests — [Reddit r/singularity](https://www.reddit.com/r/singularity/comments/1oqrhtu/openai_does_not_appear_to_be_applying_watermarks/) (excerpt; anecdotal, unverified)
- SynthID embeds its signal in pixels, while Apple Reference Image uses metadata — [Nieman Lab](https://www.niemanlab.org/2026/09/apple-launches-a-new-way-to-prove-a-photo-was-shot-with-an-iphone-not-generated-by-ai/)
- Commercial and open-source tools now advertise removal of SynthID (image and Veo video) and C2PA — e.g., [SoftOrbits](https://www.softorbits.net/ai-watermark-remover/), [removesynthid.io](https://removesynthid.io/), [GitHub remove-ai-watermarks](https://github.com/wiltodelta/remove-ai-watermarks) (excerpts). The GitHub tool's own notes show mixed results: some candidates went SynthID-negative in Gemini's verifier, while a Veo sample was still detected — [GitHub](https://github.com/wiltodelta/remove-ai-watermarks) (excerpt). Removal sites themselves concede SynthID "is designed to be robust" and removal is "probabilistic" — [removesynthid.io](https://removesynthid.io/)
- "SynthID detection is mostly internal to Google, so treat any third-party SynthID check as a rough signal" — [SoftOrbits](https://www.softorbits.net/ai-watermark-remover/) (excerpt; vendor of removal tool)

### Inferences
- A no-AI app should check for C2PA "AI-generated" assertions, IPTC digital-source-type, and any accessible pixel watermark (SynthID via a Google API, if available to third parties) as cheap auto-reject signals. Absence of a watermark carries no information.
- Open-weight generators and watermark removers mean adversarial users can always produce unmarked AI content.

### Gaps
- No source retrieved on **Meta Video Seal** robustness or adoption.
- No source confirming whether Google's SynthID Detector is available as a third-party API (vs. a portal) as of Nov 2026.
- No neutral, quantitative robustness study of SynthID vs. removal attacks retrieved.

## 5. Edge cases: computational photography, built-in AI edits, filters, captions — where is the line?

### Takeaway
Definitional ambiguity is the central enforcement problem. Every modern phone photo is ML-processed. OEM tools (Magic Eraser, Galaxy AI, Apple Clean Up, Photoshop Generative Fill) blur "edit" vs. "generate." Meta's 2024 experience shows that tagging minor AI edits angers real photographers, while fully synthetic images still slip through. Detectors disagree on lightly edited images (27–93% flag rates on the same set).

### Cited Findings
- In 2024 Meta applied "Made with AI" to real photos (e.g., a Kolkata Knight Riders IPL photo, a Pete Souza photo), apparently triggered when photographers used tools like Adobe Generative Fill to remove objects. Meantime "plenty of photos… clearly AI-generated" went unlabeled. Meta said it would make "labels reflect the amount of AI used in an image" — [TechCrunch, June 21, 2024](https://techcrunch.com/2024/06/21/meta-tagging-real-photos-made-with-ai/)
- Some photographers argued any AI tool use should be disclosed, others that editing shouldn't trigger a label. Meta then had no separate label for cleanup vs. creation — [TechCrunch](https://techcrunch.com/2024/06/21/meta-tagging-real-photos-made-with-ai/)
- Meta later moved the label for AI-*edited* content to the post menu (Sept 2024) — [Lumethic (vendor)](https://www.lumethic.com/en/articles/content-credentials-social-media-platforms) (excerpt)
- Samsung attaches C2PA plus a visible watermark specifically to Galaxy AI–edited images — [Lumethic (vendor)](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials). Google Photos records AI edits in the credential chain — [same](https://www.lumethic.com/en/articles/smartphones-c2pa-content-credentials)
- NewsGuard's lightly-edited set was flagged as AI by 27% (Hive, Sightengine) up to 93% (ScamAI) — detectors embody different implicit definitions — [NewsGuard](https://www.newsguardtech.com/special-reports/leading-ai-image-detection-tools-mislead-online-users-often-declaring-authentic-content-fake/)

### Inferences
- A workable policy needs an explicit taxonomy, for example:
  - **Allowed**: sensor and computational pipeline (HDR, Night Sight, Deep Fusion, denoise, portrait-mode blur), standard exposure/color/crop.
  - **Disputed**: generative object removal (Magic Eraser/Clean Up/Generative Fill), AI upscaling, AI sky replacement, generative beauty filters / face reshaping, AR lenses.
  - **Banned**: text-to-image/video, image-to-image restyling, generative expand, face swaps.
  - AI-assisted *captions* are text, not media; a media-focused policy could exclude them or require a disclosure.
- Technical enforcement of the "disputed" tier is weak. Pixel and Samsung record AI edits in C2PA, but iPhone Clean Up leaves no C2PA trail (iPhones have none). Detectors are unreliable on light edits. So "absolutely no AI" collapses in practice to "no *substantially* generated content," enforced by policy plus review.
- The in-app camera (Section 2) can block disputed edits by disallowing imports. That trades away editing freedom.
- Beauty filters: if the app ships its own non-generative filters (LUTs/geometric), it controls the line. Third-party generative beauty filters on imports are hard to detect.

### Gaps
- No source retrieved documenting whether Apple Clean Up / Image Playground outputs carry any marker (IPTC/EXIF) on non-18-Pro iPhones.
- No research found quantifying how often everyday phone photos contain generative edits.

## 6. Human moderation, community reporting costs, false-accusation harms

### Takeaway
Human review is needed to adjudicate detector flags and user reports, and AI-vs-human judgments are hard even for experts. False accusations against real artists are well documented (r/Art 2023, Cara 2024, Procreate/D&D artists). They cause bans, harassment and the need for timelapse "proof," which is a serious reputational risk for a no-AI app whose core users are human creators.

### Cited Findings
- r/Art banned artist Ben Moran for allegedly AI-generated work on a book cover they said took 100 hours. On appeal, the moderator "doubled down, called them a liar and insulted their art" — [BuzzFeed News](https://www.buzzfeednews.com/article/chrisstokelwalker/art-subreddit-illustrator-ai-art-controversy)
- On Cara (the anti-AI artist platform that surged in 2024), "2 or 3 artists" complained of being banned after false flags — [Reddit r/DefendingAIArt](https://www.reddit.com/r/DefendingAIArt/comments/1da6ctq/cara_was_doomed_to_fail_from_the_beginning/) (excerpt; partisan, anecdotal source)
- Artists post timelapses to rebut accusations and report lasting anxiety: "I took a break from art for months and still struggle with anxiety after being accused of AI" — [Reddit r/ProCreate](https://www.reddit.com/r/ProCreate/comments/1tjv0kl/just_to_combat_the_ai_accusations_3_this_is_the/) (excerpt); a D&D Player's Handbook artist published drafts/WIP to rebut AI accusations — [Reddit r/dndnext](https://www.reddit.com/r/dndnext/comments/18lf78x/artist_accused_of_ai_art_in_new_phb_provides/) (excerpt); "False AI accusations are destroying real creative work" — [Reddit r/gamedev](https://www.reddit.com/r/gamedev/comments/1m46xk5/false_ai_accusations_are_destroying_real_creative/) (excerpt)
- NewsGuard warns that detector false positives let "bad actors… dispute reality by citing detection tools to argue that real images are fake," and recommends human verification combining detection with reverse image search, metadata, source and contextual checks — [NewsGuard](https://www.newsguardtech.com/special-reports/leading-ai-image-detection-tools-mislead-online-users-often-declaring-authentic-content-fake/)

### Inferences
- Community reporting on a no-AI app will likely be weaponized (rivals mass-reporting "it looks AI"). This calls for reporter reputation weighting, rate limits, and a protected appeal path where creators can submit evidence (RAW files, C2PA originals, process timelapses, layered PSD/Procreate files).
- Verification badges based on attested capture or valid C2PA could shield creators from accusations. This is a product benefit of provenance even with limited coverage.
- Human review is expensive (see Gaps), so the system should route only borderline detector scores and credible reports to humans.

### Gaps
- **No sourced figures retrieved for per-item human moderation cost** or moderator throughput for AI-authenticity review (as opposed to general content moderation). This gap needs filling from another source (e.g., BPO pricing, Meta/TikTok transparency reports).
- No published data on Cara's actual moderation process, false-positive rate, or detector vendor (Cara reportedly used Hive in 2024 per general knowledge, but this was not verified in this session).
- No study found that measures human expert accuracy at distinguishing 2025–2026 generator output from real photos.
