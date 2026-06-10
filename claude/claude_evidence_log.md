# Claude Evidence Log — EDC Email Validation

Researcher: claude · Date: 2026-06-09 · Phase 1 (Domain + Naming Convention) · TEST BATCH: records R01–R11 only.

Scope note: this is a test run of Phase 1 on the first 11 records. Columns 4–13 are filled for R01–R11. R12–R55 are not yet researched. Every evidence URL below was opened in-session unless explicitly marked as surfaced via search snippet.

---

## R01 — Alabama — The Alabama Development Fund (Alabama Department of Commerce)

**Domain.** Website is madeinalabama.com, but every individual staff address on the official staff directory is @commerce.alabama.gov. Email domain != website domain.
- Source (T1): https://www.madeinalabama.com/resources/staff-directory/

**Naming convention.** Derived from published addresses on that directory:
- ellen.mcnair@commerce.alabama.gov (Ellen McNair) → first.last
- erika.mckay@commerce.alabama.gov (Erika McKay) → first.last
- brandi.boswell@commerce.alabama.gov (Brandi Boswell) → first.last
3+ matching samples → convention_confidence 90. General address contact@madeinalabama.com is in the page footer (for Phase 2).

---

## R02 — Alaska — Dept. of Commerce, Community, and Economic Development

**Domain.** Website is commerce.alaska.gov; individual staff use @alaska.gov.
- Source (T1, page revised 2026-01-22): https://www.commerce.alaska.gov/web/dcra/ServeAlaska/ContactUs.aspx

**Naming convention.**
- katie.abbott@alaska.gov (Katie Abbott) → first.last
- carla.burkhead@alaska.gov (Carla Burkhead) → first.last
- (functional: serve.alaska@alaska.gov; dcced.commissioner@alaska.gov)
2 matching personal samples + 1 functional → convention_confidence 90.
Note: a search snippet for this page showed a now-replaced staffer (jill.furbish); the live fetch showed lily.tegner. Confirms the value of fetching over trusting snippets.

---

## R03 — American Samoa — Department of Commerce  [LOW CONFIDENCE / FLAGGED]

**Domain.** Two domains in play. General/contact uses @doc.as (info@doc.as, legacy). Individual staff use @doc.as.gov.
- Director email (T3, official territory directory): lina.petaia@doc.as.gov — https://www.americansamoa.gov/directors
- Functional on DOC own site (T1): americansamoastatistics@doc.as.gov — https://www.doc.as.gov/

**Naming convention.** Only one personal-name sample (lina.petaia → first.last). The official contact page (https://www.doc.as.gov/contact) is a web form with no published staff emails. Per rubric, 1 sample caps convention_confidence at 35. Tentative pattern first.last.
Flag: resolve the @doc.as vs @doc.as.gov split and find a 2nd personal sample in Phase 5.

---

## R04 — Arizona — Arizona Commerce Authority  [CONVENTION CORRECTION]

**Domain.** azcommerce.com. Staff emails on the official Contact Us page are Cloudflare-encoded mailto links; decoded in-session.
- Source (T1): https://www.azcommerce.com/about-us/contact-us/

**Naming convention — decoded.**
- Jena (McGovern) → jenam@azcommerce.com
- Alyssa (Tufts) → alyssat@azcommerce.com
- Ryan (Ruiz) → ryanr@azcommerce.com
Pattern = firstname + last-initial. 3 matching → convention_confidence 90.
**Correction:** input guessed sandra.watson@azcommerce.com (first.last). Convention predicts sandraw@azcommerce.com. Verify in Phase 4.

---

## R05 — Arkansas — Arkansas Economic Development Commission  [CONVENTION CORRECTION]

**Domain.** arkansasedc.com. Emails on the official Leadership page are Cloudflare-encoded; decoded in-session.
- Source (T1): https://www.arkansasedc.com/leadership

**Naming convention — decoded.**
- Clint O'Neal → coneal@arkansasedc.com
- Jennifer Emerson → jemerson@arkansasedc.com
Pattern = first-initial + last. 2 matching → convention_confidence 75.
Also decoded the media-inquiries link → info@arkansasedc.com (general address, for Phase 2).
**Correction:** input guessed clint.oneal@arkansasedc.com. Decoded actual is coneal@arkansasedc.com. Verify in Phase 4.

---

## R06 — California — GO-Biz

**Domain.** Website is business.ca.gov; staff email domain is gobiz.ca.gov.
- Source (T2, official CA State Controller Personnel Office Directory PDF, updated 2026-04-07): https://www.sco.ca.gov/Files-PPSD/CPOD/governors_office_of_business.pdf

**Naming convention.**
- tami.belknap@gobiz.ca.gov, michelle.dumpit@gobiz.ca.gov, jenny.fitzgerald@gobiz.ca.gov, anulika.white@gobiz.ca.gov, chen.chong@gobiz.ca.gov → all first.last
3+ matching on an official document → convention_confidence 90.
Note: Director is Dee Dee Myers (two-word first name); verify dee.myers@ vs deedee.myers@ in Phase 4.

---

## R07 — Colorado — OEDIT  [LOW CONFIDENCE / FLAGGED]

**Domain.** state.co.us. Confirmed only via functional addresses:
- oedit.info@state.co.us (on every staff/contact page, T1): https://oedit.colorado.gov/mike-landes
- oedit_sfadmin@state.co.us (OEDIT Salesforce portal, T1): https://oedit.my.salesforce-sites.com/oedit/

**Naming convention — UNVERIFIED.** OEDIT staff bio pages hide each person's address behind a JavaScript "Email [First name]" button; the raw address is not in the served HTML/markdown. PR is outsourced: the colorado.com media room contacts decode to @handlebarpr.com (e.g., carly@handlebarpr.com), not state.co.us. No personal-name @state.co.us sample found. Convention assumed first.last (Colorado statewide standard) but unproven for this org → convention_confidence 5.
Flag: retry via an OEDIT press release media contact (typically alissa.johnson@state.co.us) in Phase 5.

---

## R08 — Connecticut — DECD

**Domain.** ct.gov. The official DECD Contact page exposes a dozen plain-text mailto links.
- Source (T1): https://portal.ct.gov/DECD/Content/About_DECD/Contact

**Naming convention.**
- patricia.paesani@ct.gov, sheila.hummel@ct.gov, binu.chandy@ct.gov, jennifer.haag@ct.gov, melinda.wilson@ct.gov → all first.last
Many matching → convention_confidence 90.
Note: full legal first names are used — "Matt" Pugliese = matthew.pugliese@ct.gov; "Mike" Wieliczka = michael.wieliczka@ct.gov. Apply legal first name in Phase 4. General DECD@ct.gov confirmed.

---

## R09 — Delaware — Division of Small Business

**Domain.** delaware.gov. Staff mailto links on official Division pages.
- Source (T1): https://business.delaware.gov/news-publications

**Naming convention.**
- andrea.wojcik@delaware.gov (opened page) → first.last
- gemini.cornish@delaware.gov (official site, https://business.delaware.gov/?p=18337) → first.last
- anastasia.jackson@delaware.gov; joe.zilcosky@delaware.gov (additional) → first.last
3+ matching → convention_confidence 90. General business@delaware.gov confirmed.
Note: input cj.bell@delaware.gov plausible, but "CJ" may be initials; verify in Phase 4.

---

## R10 — Florida — FloridaCommerce  [LOW CONFIDENCE / FLAGGED]

**Domain.** commerce.fl.gov. Confirmed only via functional addresses on official sites:
- OIG@commerce.fl.gov — https://floridajobs.org/office-directory/office-of-the-inspector-general/contact-information
- CustomerInfoCenter@commerce.fl.gov — Employ Florida help desk
- media@commerce.fl.gov — press office, https://selectflorida.org/news-resources/

**Naming convention — UNVERIFIED.** Only functional addresses are published. Florida posts a public-records notice that discourages publishing personal email; no personal-name @commerce.fl.gov sample found. Convention assumed first.last but unproven → convention_confidence 5. Domain evidence here is from official-site search results, not deep-fetched.
Flag: retry via an org chart or report PDF in Phase 5.

---

## R11 — Georgia — Georgia Dept. of Economic Development  [CONVENTION CORRECTION]

**Domain.** georgia.org.
- Official media-contacts page (T1): https://georgia.org/media-contacts
- GEDA research directory (T3): https://www.geda.org/research

**Naming convention.**
- Stefanie Harper → sharper@georgia.org (official media page)
- Dana Brewer → dbrewer@georgia.org (GEDA)
- David Denison → ddenison@georgia.org (GEDA)
Pattern = first-initial + last. 3 matching → convention_confidence 90.
**Correction:** input guessed pat.wilson@georgia.org (first.last). Convention predicts pwilson@georgia.org. Verify in Phase 4.
Note: the web fetch tool masked emails on the media page as redacted; sharper@ was confirmed via the page content surfaced in search.

---

### Phase 1 test summary (R01–R11)
- High confidence (90), convention proven: R01, R02, R06, R08, R09, R11.
- Moderate (75): R05.
- Low / unverified (5–35), flagged for retry: R03 (35), R07 (5), R10 (5).
- Convention differs from the input's first.last assumption in 3 of 11: R04 (firstname+lastinitial), R05 and R11 (firstinitial+last). This is the single most important early finding — the input email guesses encode the wrong pattern for these orgs.
- Domain != website domain in several: R01, R02, R06 (and R03 split).

---

## R12 — Guam — Guam Economic Development Authority (GEDA)  [LOW CONFIDENCE / OFFICEHOLDER FLAG]

**Domain.** investguam.com.
- Personal sample (T2, official Governor of Guam press release, Oct 2025): mary.camacho@investguam.com (Mary Camacho, Marketing & Communications Officer) — https://governor.guam.gov/press_release/geda-celebrates-60-years-of-building-guams-economy-honoring-our-legacy-investing-in-tomorrow/
- Functional on the GEDA own site: social@, help@, smallbusiness@, procurement@, qcgrants@investguam.com

**Naming convention.** Only one personal-name sample (mary.camacho -> first.last). The official Employee Directory (investguam.com/employee-directory) lists names + phone extensions but NO emails. 1 sample -> convention_confidence 35.
Officeholder flag (Phase 3): the directory and the Oct 2025 release name Christina Garcia as Administrator, not the input's Melanie Mendiola.

---

## R13 — Hawaii — DBEDT  [LOW CONFIDENCE / FLAGGED]

**Domain.** dbedt.hawaii.gov.
- Functional (official State of Hawaii agency portal, T2): director@dbedt.hawaii.gov — https://portal.ehawaii.gov/government/departments-and-agencies/
- Functional: webmaster@dbedt.hawaii.gov

**Naming convention — UNVERIFIED.** DBEDT press releases list media contacts by name + phone only (Seth Colby, Laci Goshi, Charlene Chan, Burt Lum); no personal emails published. Only functional addresses found -> convention_confidence 5.
Note: the input leadership email dbedt.director@dbedt.hawaii.gov differs from the official general inbox director@dbedt.hawaii.gov.

---

## R14 — Idaho — Idaho Department of Commerce

**Domain.** commerce.idaho.gov. Multiple plain-text staff emails on the official Contact Us page (served via the commerce.dcclients.com CMS mirror).
- Source: https://commerce.dcclients.com/contact-us/

**Naming convention.**
- matt.borud@, jake.reynolds@, tom.kealey@, debbie.green@, carmen.achabal@, taylor.walker@commerce.idaho.gov -> all first.last; jennifer.verdon@commerce.idaho.gov (T3 trade listing)
3+ matching -> convention_confidence 90. General info@commerce.idaho.gov.
Note: input tom.kealey@ matches; verify Tom Kealey is still Director in Phase 3.

---

## R15 — Illinois — DCEO

**Domain.** illinois.gov. Official DCEO Contact Us page exposes plain-text emails.
- Source (T1): https://dceo.illinois.gov/oe3/contact-us.html

**Naming convention.**
- Diana.Alfaro@, Becky.Blankenship@illinois.gov -> first.last; additional Erin.Guthrie@, Crystal.Bigelow@, susan.boggs@, chris.sedgwick@illinois.gov
3+ matching -> convention_confidence 90.
Note: some staff use first.middleinitial.last to disambiguate (Rebecca.J.Bailey@, mark.a.burgess@). Input kristin.richards@ matches; Kristin Richards listed as Director.

---

## R16 — Indiana — IEDC

**Domain.** iedc.in.gov. Official Contact page exposes plain-text emails.
- Source (T1): https://iedc.in.gov/contact

**Naming convention.**
- LJagger@ (Lindsay Jagger), RColbert@ (Renia Colbert), SSalisbury@ (Sarah Salisbury), ALendy@ (Andrea Lendy), MWasky@iedc.in.gov -> first-initial + last
3+ matching -> convention_confidence 90.
Exceptions: first-two-letters+last (romartin@ for Roy Martin); numeric suffix for collisions (CBarton1@, NKim1@). Overseas trade offices use @investindiana.com. General iedc@; portal help iedchelp@iedc.in.gov.
Officeholder note (Phase 3): Secretary of Commerce now David Rosenberg under Gov. Braun; Wikipedia still lists Bradley Chambers.

---

## R17 — Iowa — Iowa Economic Development Authority  [LOW CONFIDENCE]

**Domain.** iowaeda.com.
- Personal sample (T3 state trade listing): peggy.kerr@iowaeda.com (first.last) — https://globaledge.msu.edu/states/iowa/tradecontacts
- Functional: director@, communications@, boardinfo@, traveliowa@iowaeda.com — https://opportunityiowa.gov/contact

**Naming convention.** One personal-name sample (peggy.kerr -> first.last). Most named staff are published with functional inboxes only. 1 sample -> convention_confidence 35. An aggregator suggests firstinitial.last as an alternate, unverified.
Note: Director Debi Durham confirmed (functional director@iowaeda.com). Public-facing portal is opportunityiowa.gov.

---

## R18 — Kansas — Kansas Department of Commerce  [DOMAIN + CONVENTION CONFLICT / FLAGGED]

**Domain.** Email domain is ks.gov, NOT the website domain (input kansascommerce.com; Wikipedia kansascommerce.gov).
- Reliable sample (T3 state trade listing): Randi.TveitaraasJack@ks.gov (Deputy Director, International) — https://globaledge.msu.edu/states/kansas/tradecontacts
- Low-trust sample (Prospeo): April.Chiang@ks.gov

**Naming convention — CONFLICT.** The one reliable sample is first.last. Aggregators disagree: ContactOut/LeadIQ claim firstinitiallast @kansascommerce.com; Prospeo claims firstinitial.last @ks.gov -> convention_confidence 35.
Flag: needs an official staff-directory fetch to resolve domain (ks.gov vs kansascommerce.com) and local-part. Secretary David Toland.

---

## R19 — Kentucky — Cabinet for Economic Development

**Domain.** ky.gov (website ced.ky.gov). The full official staff directory lists dozens of emails (opened in-session).
- Source (T1): https://newkentuckyhome.ky.gov/Home/Staff (ced.ky.gov/Home/Staff redirects here)

**Naming convention.**
- Jeff.Noel@ (Secretary), Kristina.Slattery@ (Commissioner), Matthew.Wingate@, Kylee.Palmer@, Andy.Luttner@ky.gov -> first.last; dozens more
Dominant first.last -> convention_confidence 90.
Exceptions: firstinitial+last (dbrock@, tbates@, MNeCamp@); first+middleinitial.last (BradleyL.Popp@, CharityM.Hedges@); trailing-initial variants (shannonn.macdonald@, Eric.Estillr@). International offices use @teamkentucky.international. General econdev@; open records CEDOpenRecords@ky.gov.
Officeholder: Secretary Jeff Noel; Commissioner Kristina Slattery (verify Phase 3).

---

## R20 — Louisiana — Louisiana Economic Development (LED)

**Domain.** la.gov (website opportunitylouisiana.com/.gov).
- Personal (T1 official LED page): Christopher.Cassagne@la.gov (Senior Director, Growth Network) — https://www.opportunitylouisiana.gov/small-business/growth-network/louisiana-growth-leaders
- Personal (T2): Janelle.Dickey@la.gov (CDBG program contact) — https://www.doa.la.gov/doa/ocd-lga/cdbg-and-cdbg-cv/lcdbg-programs/economic-development/

**Naming convention.** 2 matching first.last samples -> convention_confidence 75. LED publishes a searchable staff directory (opportunitylouisiana.gov/contact-us) to lift to 90 later. Functional LED@; LEDPublicRecords@la.gov.
Officeholder: Secretary Susan B. Bourgeois.

---

## R21 — Maine — DECD

**Domain.** maine.gov. Multiple staff emails on official maine.gov/decd pages.
- Sources (T1): https://www.maine.gov/decd/community-development/contact ; https://www.maine.gov/decd/about

**Naming convention.**
- deborah.johnson@, brianne.hasty@, sharon.l.thomas@ (contact page); phoenix.mclaughlin@maine.gov (About page) -> first.last
3+ matching -> convention_confidence 90.
Note: some staff include a middle initial (sharon.l.thomas@). Functional: business.answers@ (general), economicplan.decd@, BizAwards.DECD@, housing.moca@maine.gov.
Officeholder: Commissioner Michael Duguay.

---

## R22 — Maryland — Maryland Department of Commerce  [CONVENTION CONFLICT]

**Domain.** maryland.gov (website commerce.maryland.gov).
- Verifiable personal sample (T3 state trade listing): signe.pringle@maryland.gov (Deputy Secretary) — https://globaledge.msu.edu/states/maryland/tradecontacts

**Naming convention — CONFLICT.** One verifiable sample is first.last. An aggregator (Prospeo) reports firstinitial.last as most common (~66%) with first.last ~27% -> convention_confidence 35. Some legacy addresses use @choosemaryland.org; collision suffixes appear elsewhere in MD state (Kelly.Charles1@maryland.gov).
Flag: needs the official commerce.maryland.gov leadership/staff directory fetch to confirm local-part.

---

### Phase 1 batch summary (R12–R22)
- High confidence (90), convention proven: R14 (Idaho), R15 (Illinois), R16 (Indiana), R19 (Kentucky), R21 (Maine).
- Moderate (75): R20 (Louisiana).
- Low / unverified (5–35), flagged: R12 (35, officeholder change flag), R13 (5), R17 (35), R18 (35, domain+convention conflict), R22 (35, convention conflict).
- Email domain != website domain again: R18 (ks.gov), R19 (ky.gov), R20 (la.gov), R22 (maryland.gov); R12 site=email (investguam.com).
- Hidden-personal-email orgs (names + phones only, functional addresses): R13 (Hawaii), partially R12 and R17 — same pattern as R07/R10 earlier.
- Officeholder discrepancies vs input surfaced for Phase 3: R12 (Garcia vs Mendiola), R16 (Rosenberg vs Chambers); also verify R14, R15, R19, R20, R21.

---

## R23 — Massachusetts — Executive Office of Economic Development

**Domain.** mass.gov. The official MOBD Regional Directors page (under EOED) exposes plain-text staff emails.
- Source (T1): https://www.mass.gov/info-details/mass-office-of-business-development-regional-directors

**Naming convention.**
- naomi.berlin@, peter.milano@mass.gov -> first.last; press contact Margaret.M.Quackenbush@ and Kevin Kuros = kevin.j.kuros@ -> first.middleinitial.last variant
3+ matching -> convention_confidence 90.
Note: general intake via the Business Front Door web form (mass.gov/bfd). Verify the current Secretary of Economic Development in Phase 3.

---

## R24 — Michigan — MEDC  [CONVENTION CORRECTION]

**Domain.** michigan.org (website michiganbusiness.org).
- Sources (T1): https://www.michiganbusiness.org/services/how-medc-can-help/ ; https://www.michiganbusiness.org/about-medc/media-room/media-contacts/

**Naming convention.** lastname + first-initial, with a numeric suffix appended for uniqueness/collisions:
- schwabv@ (Vicki Schwab), holtzp@ (Paula Holtz), blackn@ (Nicole Black), breithauptt@ (Tino Breithaupt) -> no suffix
- emersond1@ (Danielle Emerson), mccauleym3@ (Matt McCauley), donaldsonc2@ (Charles Donaldson), jordand4@ (Damon Jordan), watsona11@ (Alison Watson), tuckerj6@ (Jennifer Tucker) -> numeric suffix
Many matching -> convention_confidence 90. Functional FOIA medcfoia@michigan.org.
**Correction:** NOT first.last. The numeric suffix is unpredictable per person; verify the leader's exact address in Phase 4.

---

## R25 — Minnesota — DEED

**Domain.** state.mn.us (website mn.gov/deed).
- Sources (T1): https://mn.gov/deed/business/financing-business/mjsp/contact/ ; https://mn.gov/deed/programs-services/trade-adjustment/contacts/

**Naming convention.**
- Paul.Moe@, Brenda.Buckles@, Jodie.Greising@, Danielle.Kressin@, carol.bisbee@, amy.carlson@, dana.dumbacher@, ed.hodder@state.mn.us -> all first.last
Many matching -> convention_confidence 90.
Exceptions: middle initial (olajide.x.williams@); hyphenated surname preserved (claudette.parchment-roehrich@). Many functional program inboxes (deed.taa@, deed.mjsp@, CareerForce@, deed.mnsbdc@state.mn.us). Verify Commissioner (Matt Varilek) in Phase 3.

---

## R26 — Mississippi — Mississippi Development Authority  [LOW CONFIDENCE / FLAGGED]

**Domain.** mississippi.org.
- Personal sample (T3 partner directory): odiaz@mississippi.org (Orlando Diaz, South American Office Director) — https://scedirectory.smartcommunityexchange.com/listing/mississippi-development-authority/

**Naming convention.** One reliable personal sample is first-initial+last. The MDA own site (mississippi.org/about/departments) hides personal emails behind Email Me JavaScript buttons (same pattern as Colorado/Florida). 1 sample -> convention_confidence 35. Aggregators agree firstinitial+last is dominant (ContactOut ~74%) with firstlast as alternate, but low-trust.
Note: Executive Director Bill Cork (verify Phase 3).

---

## R27 — Missouri — Department of Economic Development

**Domain.** ded.mo.gov.
- Sources (T1): the official DED Submittable application portal (https://missouridepartmentofeconomicdevelopment.submittable.com/submit) and the official DED LinkedIn.

**Naming convention.**
- harry.bozoian@, debbie.feeback@ded.mo.gov (application portal); Olivia.Ross@ded.mo.gov (official LinkedIn); amelia.aubuchon@ded.mo.gov (MGISAC) -> all first.last
3+ matching -> convention_confidence 90. General ecodev@ded.mo.gov; program inboxes redevelopment@, htc@, mdfb@ded.mo.gov.
Officeholder: Acting Director Michelle Hataway per Wikipedia; an older release named Maggie Kost as Acting Director — leadership in flux, verify Phase 3.

---

## R28 — Montana — Department of Commerce

**Domain.** mt.gov (website commerce.mt.gov).
- Source (T1): https://commerce.mt.gov/about/leadership

**Naming convention.**
- marta.bertoglio@, mandy.rambo@, mitch.staley@, cheryl.cohen@mt.gov -> all first.last
3+ matching -> convention_confidence 90.
Exceptions: firstinitial+last (adeyoung@mt.gov for Angie DeYoung, trade office; jpelej@mt.gov in the state directory).
Officeholder: Director Marta Bertoglio confirmed on the Leadership page (verify still current in Phase 3).

---

## R29 — Nebraska — Department of Economic Development

**Domain.** nebraska.gov (website opportunity.nebraska.gov).
- Personal (T1 official DED Contact page): kate.ellingson@nebraska.gov (media contact) — https://opportunity.nebraska.gov/contact/
- Personal (T1 official AmpliFund grant listing): kimberly.jasa-harris@nebraska.gov (agency contact, hyphenated surname preserved) — https://ne.amplifund.com/Public/Opportunities/Details/f53fa306-0a4d-49e5-95b2-bc45eabbb8e6

**Naming convention.** 2 matching first.last samples -> convention_confidence 75. General DED.ImagiNE@nebraska.gov. DED publishes a Field Staff map/list that could lift to 90 later.
Note: verify Director in Phase 3.

---

## R30 — Nevada — GOED  [DOMAIN CONFLICT / FLAGGED]

**Domain.** Website diversifynevada.com; the agency also runs goed.nv.gov.
- Functional general inbox (official GOED Facebook): goed@goed.nv.gov — https://www.facebook.com/NevadaGOED/

**Naming convention — UNVERIFIED.** No personal staff email is published (contact pages are web forms; the staff-directory page lists no emails). Aggregators claim firstinitial+last @diversifynevada.com (RocketReach 100%; Prospeo ~67%) but low-trust and possibly stale (predating the goed.nv.gov move). Domain conflict goed.nv.gov vs diversifynevada.com -> convention_confidence 5.
Note: Executive Director Tom Burns (verify Phase 3).

---

## R31 — New Hampshire — Dept. of Business and Economic Affairs  [DOMAIN + CONVENTION CONFLICT / FLAGGED]

**Domain.** Email domain appears to be livefree.nh.gov, not the website (nheconomy.com / dbea.nh.gov).
- Aggregator (ZoomInfo, masks local part): l***@livefree.nh.gov (Lorna Colquhoun, Deputy Director Public Affairs) — https://www.zoominfo.com/p/Lorna-Colquhoun/12045012688
- General (official): info@nheconomy.com

**Naming convention — UNVERIFIED.** The official Meet the Staff page lists names + phones only (hidden-email pattern). Prospeo reports two conflicting formats: firstnamelastname (~54%) and first.last (~46%) @livefree.nh.gov. No reliable personal sample -> convention_confidence 5.
Officeholder: Commissioner Lucy Lange (Taylor Caswell resigned Oct 2025); verify Phase 3.

---

## R32 — New Jersey — NJEDA  [DOMAIN + CONVENTION CONFLICT / FLAGGED]

**Domain.** Splits between njeda.gov and njeda.com.
- Functional (official, T1): oprae-mail@njeda.gov — https://www.njeda.gov/public_information/ ; NJBASE@, smallbusinessservices@, languagehelp@njeda.gov; general CustomerCare@njeda.com — https://www.njeda.gov/about/

**Naming convention — UNVERIFIED.** Official pages publish only functional addresses. No personal staff email published; aggregators conflict (Prospeo: firstinitial+last @njeda.com ~49%, first.last @njeda.gov ~24%, firstinitial.last @njeda.gov ~21%; SignalHire shows @njeda.gov but masks local parts) -> convention_confidence 5.
Officeholder: CEO Tim Sullivan; Chief of Staff Emma Corrado (verify Phase 3).

---

## R33 — New Mexico — Economic Development Department

**Domain.** edd.nm.gov (website edd.newmexico.gov).
- Source (T1): https://www.edd.newmexico.gov/contact-us/

**Naming convention.**
- Jennifer.Myers@, Rebecca.Hansana@, Yuriria.Morales@edd.nm.gov (official Contact page) -> first.last; keegan.mackenzie-chavez@edd.nm.gov (official LinkedIn, hyphenated surname preserved)
3+ matching -> convention_confidence 90. General info@edd.nm.gov (also edd.info@edd.nm.gov; info@edd.newmexico.gov).
Officeholder: Cabinet Secretary Rob Black; Deputy Secretary Isaac Romero (verify Phase 3).

---

### Phase 1 batch summary (R23–R33)
- High confidence (90), convention proven: R23 (Massachusetts), R24 (Michigan), R25 (Minnesota), R27 (Missouri), R28 (Montana), R33 (New Mexico).
- Moderate (75): R29 (Nebraska).
- Low / unverified (5–35), flagged: R26 (35, hidden emails), R30 (5, domain conflict), R31 (5, domain+convention conflict), R32 (5, domain+convention conflict).
- CONVENTION CORRECTION (not first.last): R24 Michigan = lastname+firstinitial with a numeric suffix — a distinct new pattern; R26 Mississippi = firstinitial+last (tentative).
- Email domain != website domain again: R24 (michigan.org), R25 (state.mn.us), R33 (edd.nm.gov); R30/R31/R32 have outright domain conflicts (goed.nv.gov, livefree.nh.gov, njeda.gov/.com).
- Hidden-personal-email orgs (functional only / Email Me buttons / names+phones): R26 (Mississippi), R30 (Nevada), R31 (New Hampshire), R32 (New Jersey) — same family as R07/R10/R13.
- Officeholder notes for Phase 3: R27 (Hataway vs older Kost), R31 (Lange; Caswell resigned). Plus verify leaders for R23, R24, R25, R28, R29, R30, R32, R33.

---

## R34 — New York — Empire State Development
- Domain: esd.ny.gov. Confirmed across many official ESD board/directors-meeting media advisories (PDFs on esd.ny.gov) carrying functional addresses PressOffice@esd.ny.gov, ESD@esd.ny.gov, NYEZC@esd.ny.gov.
- Evidence URL: https://esd.ny.gov/sites/default/files/media/document/ESD-Directors-Meeting-11526.pdf
- Convention: first.last (strong aggregator convergence; NO plain personal sample published this session). Confidence 40 (two functional samples that confirm the domain but not a personal pattern; aggregators agree first.last but uncorroborated by a real personal address).
- Samples: PressOffice@esd.ny.gov and ESD@esd.ny.gov (both functional, same PDF).
- Notes: web_fetch of the esd.ny.gov homepage REDACTS emails to [email protected]; ZoomInfo masks Chief of Staff Noah Rayman as n***@esd.ny.gov. CEO Hope Knight (verify Phase 3). Retry a staff bio or press release for a personal-name sample to lift to 75–90.

## R35 — North Carolina — EDPNC
- Domain: edpnc.com. Multiple staff personal emails on the official EDPNC site (Logic Leads to North Carolina page).
- Evidence URL: https://edpnc.com/logic/
- Convention: first.last. Confidence 90 (3+ matching samples: melissa.smith@, austin.rouse@, dylan.finch@, tim.feltz@).
- Samples: melissa.smith@edpnc.com and austin.rouse@edpnc.com (same page).
- Notes: RocketReach agrees first.last (~93.7%). Functional cir@edpnc.com. CEO Christopher Chung (verify Phase 3).

## R36 — North Dakota — Department of Commerce
- Domain: nd.gov (email domain; website commerce.nd.gov). ND uses a single statewide nd.gov mail system.
- Evidence URL: https://ednd.org/listing/north-dakota-department-of-commerce-6/ (ND Commerce staff email rgarman@nd.gov on the EDND partner directory).
- Convention: firstinitial+last. Confidence 75 (one strong real sample plus the known statewide nd.gov pattern; variants include first+middleinitial+last, so collisions are unpredictable).
- Sample: rgarman@nd.gov. No clean second personal sample surfaced this session (cols 11–12 left blank).
- Notes: Director Katie Ralston Howe; Deputy Director Tracey Miller (verify Phase 3).

## R37 — Northern Mariana Islands — Department of Commerce
- DOMAIN CORRECTION: email domain is commerce.gov.mp (input website listed commerce.cnmi.gov).
- Evidence URL: https://www.commerce.gov.mp/ (official site general info@commerce.gov.mp); registrar portal role-based registrar.reyes@commerce.gov.mp at https://registrar.cnmi.gov/.
- Convention: UNVERIFIED. Confidence 25 (only functional/role-based addresses; no personal-name sample).
- Samples: info@commerce.gov.mp and registrar.reyes@commerce.gov.mp.
- Notes: the official Our Team / Office of the Secretary pages are Lorem Ipsum placeholder content. Secretary Mark O. Rabauliman (verify Phase 3).

## R38 — Ohio — Department of Development
- Domain: development.ohio.gov. Two ODOD staff emails on the official Ohio APEX Accelerator contact page.
- Evidence URL: https://find.govcontracts.ohio.gov/contact/
- Convention: first.last. Confidence 75 (two matching real samples).
- Samples: joseph.scott@development.ohio.gov and dasia.johnson@development.ohio.gov (same page).
- Notes: Director Lydia Mihalik (verify Phase 3).

## R39 — Oklahoma — Department of Commerce
- Domain: okcommerce.gov. ray.little on the Oklahoma.gov business contact page; jared.cooper on the official ODOC LinkedIn.
- Evidence URL: https://oklahoma.gov/business/help/contact.html
- Convention: first.last. Confidence 75 (two matching real samples on official sources). RocketReach agrees first.last (~50%); Prospeo first_last underscore appears to be an artifact.
- Samples: ray.little@okcommerce.gov (contact page) and jared.cooper@okcommerce.gov (ODOC LinkedIn).
- Notes: general hello@okcommerce.gov; recruiting Recruiter@okcommerce.gov. Executive Director Brent Kisling; Secretary of Commerce Sean Kouplen (verify Phase 3).

## R40 — Oregon — Business Oregon
- Domain: biz.oregon.gov (email domain; website oregon.gov/biz).
- Evidence URL: https://www.oregon.gov/biz/aboutus/pages/rules.aspx (staff email on the official Business Oregon Statutes & Rules page).
- Convention: first.last, frequently first.middleinitial.last. Confidence 75.
- Samples: Marjorie.Waniata@biz.oregon.gov (official page) and Janeen.M.HILBRINK@biz.oregon.gov (OEDA member directory, https://oeda.biz/member-directory/).
- Notes: functional Business.OREGON_INFO@biz.oregon.gov. Statewide oregon.gov first.last corroborates. Director Sophorn Cheang (verify Phase 3).

## R41 — Pennsylvania — DCED
- Domain: pa.gov (email domain; websites dced.pa.gov / newpa.com differ).
- Evidence URL: https://dced.pa.gov/housing-and-development/community-planning/ (multiple DCED staff emails).
- Convention: firstinitial+last (NOT first.last). Confidence 90 (3+ matching samples: lmroszczyk, ncannistra, rschoenly; dbriel for the trade office).
- Samples: lmroszczyk@pa.gov and ncannistra@pa.gov (same page).
- Notes: long surnames are truncated (Mroszczyk-Murphy -> lmroszczyk; Cannistraci -> ncannistra) — confirm per person in Phase 4. Functional RA-DCEDHousingPlan@pa.gov. Secretary Rick Siger (verify Phase 3).

## R42 — Puerto Rico — DDEC
- Domain: ddec.pr.gov (confirmed via the official .pr.gov acceso-informacion page).
- Evidence URL: https://www.desarrollo.pr.gov/acceso-informacion
- Convention: UNVERIFIED. Confidence 25 (only functional addresses surfaced; no personal-name sample).
- Samples: transferencia.electronicas@ddec.pr.gov (official page) and promoexport@ddec.pr.gov (trade office, https://www.sba.gov/event/65715).
- Notes: ZoomInfo masks personal local parts (****@ddec.pr.gov). SignalHire claims an unusual lastNameInitial_firstName format (d_jane@, ~62%) — low-trust, uncorroborated. Spanish-language agency; compound surnames likely affect the local-part. Secretary Sebastian Negron Reichard per Wikipedia — verify current status in Phase 3 (possible recent change).

## R43 — Rhode Island — Rhode Island Commerce
- Domain: commerceri.com (quasi-public agency).
- Evidence URL: https://globaledge.msu.edu/states/rhode-island/tradecontacts (Katherine Therieau, Director International Trade Programs: ktherieau@commerceri.com).
- Convention: firstinitial+last OR firstinitial.last — CONFLICT. Confidence 35.
- Samples: ktherieau@commerceri.com (trade-contacts listing) and info@commerceri.com (official contact-us page).
- Notes: the one real published personal sample is ktherieau@ (firstinitial+last, NO dot), but Prospeo favors the dotted firstinitial.last form k.therieau@ (86.3%) over first.last (11.8%) and ktherieau no-dot (2%). Functional MainStreet@commerceri.com. ZoomInfo masks Gabriela Gutierrez (g***@). RI Commerce Secretary/CEO not captured this session (verify Phase 3).

## R44 — South Carolina — Department of Commerce
- Domain: sccommerce.com (email domain = website domain).
- Evidence URL: https://www.sccommerce.com/sites/default/files/2019-07/SCBusinessResources.pdf (official SC Business Resource Guide PDF; Ashely Teasdel, Manager of Small Business: ateasdel@sccommerce.com).
- Convention: firstinitial+last (NOT first.last, NOT dotted). Confidence 75 (two matching real samples).
- Samples: ateasdel@sccommerce.com (official PDF) and nconwell@sccommerce.com (Nancy Conwell, Innovation Ecosystem Manager, on the SC Commerce Innovation Team resource page, https://www.abbevillecitysc.com/553/SC-Commerce-Business-Resources).
- Notes: RocketReach 93.9% firstinitial+last and Highperformr 85% corroborate; SignalHire's firstName.lastNameInitial (jane.d, 60%) conflicts and is low-trust/uncorroborated. Could lift to 90 with a third official sample. General info@sccommerce.com; functional LocateSC@, SmallBizSupport@. Secretary of Commerce (verify Phase 3).

---

## Phase 1 batch summary (R34–R44)
- High confidence (90), convention proven: R35 (North Carolina, edpnc.com), R41 (Pennsylvania, pa.gov firstinitial+last).
- Moderate (75): R36 (North Dakota, nd.gov firstinitial+last), R38 (Ohio, development.ohio.gov first.last), R39 (Oklahoma, okcommerce.gov first.last), R40 (Oregon, biz.oregon.gov first.last), R44 (South Carolina, sccommerce.com firstinitial+last).
- Low / unverified, flagged: R34 (40, NY — functional only, aggregators agree first.last but no personal sample), R37 (25, NMI — placeholder Our Team pages), R42 (25, PR — functional only), R43 (35, RI — dot-vs-no-dot conflict).
- DOMAIN CORRECTION: R37 Northern Mariana Islands email domain is commerce.gov.mp, not the input's commerce.cnmi.gov.
- Email domain != website domain again: R36 (nd.gov vs commerce.nd.gov), R40 (biz.oregon.gov vs oregon.gov/biz), R41 (pa.gov vs dced.pa.gov/newpa.com).
- Convention is firstinitial+last (NOT first.last) for R36, R41, R44 — continue to test each domain rather than assuming first.last.
- Hidden / functional-only orgs (no personal sample this session): R34 (NY), R37 (NMI), R42 (PR) — same family as R07/R10/R13/R26/R30/R31/R32. web_fetch redaction observed again at R34 (esd.ny.gov homepage masks emails to [email protected]).
- Officeholder verification for Phase 3: R36 (Howe/Miller), R37 (Rabauliman), R42 (Negron Reichard — possible recent change), R43 (Secretary/CEO not captured). Plus CEO/Director verify for R34 (Knight), R35 (Chung), R38 (Mihalik), R39 (Kisling/Kouplen), R40 (Cheang), R41 (Siger), R44.

---

## R45 — South Dakota — Governor's Office of Economic Development
- Domain: SPLIT. Website/marketing sdgoed.com; official state mail state.sd.us; trade office sdreadytowork.com.
- Evidence URL: https://sdgoed.com/partners/governors-conference-on-economic-development2026/ (lexie.warejcka@sdgoed.com, first.last).
- Convention: first.last (tentative). Confidence 40 (one real personal sample at the marketing domain; aggregator conflicts; domain split).
- Samples: lexie.warejcka@sdgoed.com (conference page) and goedinfo@state.sd.us (functional, official contact-us page). Trade office travis.dovre@sdreadytowork.com (first.last) on the globalEDGE listing.
- Notes: Prospeo claims firstinitial.last (j.doe@sdgoed.com) dominant (64.7%) over first.last (35.3%), conflicting with the one real sample. OFFICEHOLDER CHANGE: Commissioner Bill Even (appointed April 2025); Joe Fiala moved to Deputy Commissioner (Yahoo/GOED news). Functional GOED.CBDGDRInfo@state.sd.us.

## R46 — Tennessee — Economic and Community Development
- Domain: tn.gov (websites tn.gov/ecd and tnecd.com).
- Evidence URL: https://www.tn.gov/ecd/small-business/tninvestco/contact-us.html (Lamont.Price@tn.gov, first.last).
- Convention: first.last. Confidence 90 (multiple real samples; Prospeo reports TNECD first.last 100%).
- Samples: Lamont.Price@tn.gov (official ECD page) and karel.abboud@tn.gov (state trade office, globalEDGE). Also john.hatfield@tn.gov (regional director).
- Notes: functional ECD.Communications.Office@tn.gov. Commissioner of ECD (verify Phase 3).

## R47 — Texas — Office of the Governor, Economic Development & Tourism
- Domain: gov.texas.gov.
- Evidence URL: https://media.governmentnavigator.com/media/bid/1770241860_2-4-26_301-26-06490_1.pdf (official OOG/EDT RFP; Michael.White@gov.texas.gov, Contract Specialist, first.last).
- Convention: first.last (one real personal sample). Confidence 40.
- Samples: Michael.White@gov.texas.gov (official RFP) and business@gov.texas.gov (functional, official EDT page).
- Notes: ZoomInfo masks Laurel Davies as l***@gov.texas.gov (consistent with first.last). Functional TexasProduct.Fund@gov.texas.gov. Could lift to 75–90 with a second personal sample. EDT sits within the Office of the Governor. Executive Director Adriana Cruz (appointed 2019; verify Phase 3).

## R48 — U.S. Virgin Islands — Economic Development Authority
- Domain: usvieda.org (confirmed via official press releases).
- Evidence URL: https://usvieda.org/press_release/us-virgin-islands-economic-development-authority-launches-usvi-online/ (info@usvieda.org).
- Convention: UNVERIFIED. Confidence 25 (only functional addresses; no personal-name sample; aggregators conflict).
- Samples: info@usvieda.org and marketing@usvieda.org (both functional).
- Notes: aggregators conflict — RocketReach 96.2% / ContactOut 100% firstinitial+last (jdoe) vs Prospeo firstnamelastname (johndoe) 60% — both no-dot. Semi-autonomous territorial authority. CEO per older 2018 press releases Kamal I. Latham (verify current Phase 3).

## R49 — Utah — Governor's Office of Economic Opportunity
- Domain: utah.gov (website business.utah.gov).
- Evidence URL: https://business.utah.gov/team/ (official Meet the Team page; many staff emails).
- Convention: firstinitial+last (predominant). Confidence 90.
- Samples: trosander@utah.gov and nrandall@utah.gov (official team page).
- Notes: VARIANTS — firstname+last for some (aspenorton@, aaronprice@) and first+middleinitial+last for collisions/short names (jrmoss@ Jefferson Moss, mtblack@, bccall@) — verify each person in Phase 4. Functional business@utah.gov. Executive Director/Commissioner Jefferson Moss; Deputy Commissioner Tara Rosander (verify Phase 3).

## R50 — Vermont — Agency of Commerce and Community Development
- Domain: vermont.gov (website accd.vermont.gov).
- Evidence URL: https://accd.vermont.gov/about-us/contact-us (elizabeth.adams@vermont.gov, first.last).
- Convention: first.last. Confidence 90 (multiple real samples across official ACCD pages).
- Samples: elizabeth.adams@vermont.gov (official Contact Us) and scott.sharland@vermont.gov (official Housing directory). Also jennifer.lavoie@, Katharine.Ingram@, Johanna.Petersen@vermont.gov.
- Notes: functional ACCD.DEDInfo@, ACCD.APEXinfo@, ACCD.CDBGDR@vermont.gov. Secretary: Wikipedia lists Patricia Moulton (stale); current chair-designating Secretary appears to be Alex Farrell (verify Phase 3).

## R51 — Virginia — Economic Development Partnership
- Domain: vedp.org (secondary marketing domain yesvirginia.org).
- Evidence URL: https://studies.virginiageneralassembly.gov/studies/256 (awescott@vedp.org, Abigail Wescott, Managing Director External Affairs).
- Convention: firstinitial+last. Confidence 75 (two matching real samples).
- Samples: awescott@vedp.org (VA General Assembly listing) and sagee@vedp.org (Stephanie Agee, state trade office, globalEDGE).
- Notes: Prospeo corroborates firstinitial+last (52.2%); SignalHire's lastName_firstName (doe_jane, 91%) conflicts and is contradicted by the real samples. CEO/President Jason El Koubi (succeeded Stephen Moret; aggregators listing Jeff Anderson / Carrie Vuori appear stale) — verify Phase 3.

## R52 — Washington — State Department of Commerce
- Domain: commerce.wa.gov (email domain = website).
- Evidence URL: https://www.commerce.wa.gov/community-engagement/regional-team/ (Martin.Sanchez@commerce.wa.gov, first.last).
- Convention: first.last. Confidence 90 (multiple real samples; ContactOut 85.29% first.last).
- Samples: Martin.Sanchez@commerce.wa.gov (regional team) and Buck.Lucas@commerce.wa.gov (local-government portal). Also Jennifer.Cole@, Mark.Calhoon@, tedd.kelleher@commerce.wa.gov.
- Notes: functional ChooseWashington@, ComCustServ@, icap@commerce.wa.gov. Director (interim) Sarah Clifthorne per Wikipedia (verify Phase 3).

## R53 — West Virginia — Department of Economic Development
- Domain: wv.gov (websites economicdevelopment.wv.gov / westvirginia.gov / wvdo.org).
- Evidence URL: https://westvirginia.gov/connect-with-us/wv-economic-development-regional-representative-map/ (Matthew.K.Borror@wv.gov, first.middleinitial.last).
- Convention: first.middleinitial.last (frequently); first.last when no middle initial. Confidence 90 (3+ matching real samples).
- Samples: Matthew.K.Borror@wv.gov and Keith.R.McIntosh@wv.gov (official regional map). Also Chris.S.Pauley@, Samantha.Smith@ (map); Taylor.S.Cole@wv.gov (WVEDA staff page).
- Notes: RocketReach reports statewide first.last 82.1% plus first.middleinitial.last. Middle-initial dependence — verify per person in Phase 4. Functional askme@wv.gov, WVOEInfo@wv.gov. Secretary/Director of Economic Development (verify Phase 3).

## R54 — Wisconsin — Economic Development Corporation
- Domain: wedc.org (email domain = website; public-private corporation).
- Evidence URL: https://wedc.org/contact-us/ (carolyn.brooks@wedc.org, first.last).
- Convention: first.last. Confidence 90 (many real samples across official pages; RocketReach 92.4% first.last).
- Samples: carolyn.brooks@wedc.org (Contact Us) and tracy.luber@wedc.org (Staff Directory). Also david.callender@, michael.ward@, nichole.crust@, francisca.rodriguez@, heather.smith@wedc.org.
- Notes: Prospeo's firstinitial.last (j.doe, 69.2%) is contradicted by the many real official samples. Functional events@wedc.org. Secretary & CEO John W. Miller per Wikipedia (ContactOut mislabels Kate Constalie as CEO — she is Senior Advisor to the CEO) — verify Phase 3.

## R55 — Wyoming — Business Council
- Domain: wyo.gov (website wyomingbusiness.org).
- Evidence URL: https://www.linkedin.com/company/wyoming-business-council (official WBC LinkedIn; kayla.kler@wyo.gov, first.last).
- Convention: first.last (numeric suffix appended on name collisions). Confidence 75 (two real samples; Prospeo 100% first.last; statewide wyo.gov corroborates).
- Samples: kayla.kler@wyo.gov (current WBC, official LinkedIn) and john.jenks1@wyo.gov (former WBC Economic Initiatives Director, Wyoming Energy Authority bio).
- Notes: NUMERIC SUFFIX on collisions (john.jenks1; statewide jason.lux1, savannah.bascus1) — verify per person in Phase 4. General info.wbc@wyo.gov. CEO Josh Dorrell (verify Phase 3).

---

## Phase 1 batch summary (R45–R55)
- High confidence (90), convention proven: R46 (Tennessee, tn.gov first.last), R49 (Utah, utah.gov firstinitial+last), R50 (Vermont, vermont.gov first.last), R52 (Washington, commerce.wa.gov first.last), R53 (West Virginia, wv.gov first.middleinitial.last), R54 (Wisconsin, wedc.org first.last).
- Moderate (75): R51 (Virginia, vedp.org firstinitial+last), R55 (Wyoming, wyo.gov first.last).
- Low / unverified, flagged: R45 (40, SD — domain split, one sample, aggregator conflict), R47 (40, TX — one personal sample), R48 (25, USVI — functional only, aggregator conflict).
- Email domain != website domain again: R45 (split sdgoed.com/state.sd.us/sdreadytowork.com), R49 (utah.gov vs business.utah.gov), R50 (vermont.gov vs accd.vermont.gov), R53 (wv.gov vs economicdevelopment.wv.gov), R55 (wyo.gov vs wyomingbusiness.org).
- Convention is firstinitial+last (NOT first.last): R49 (predominant), R51.
- New convention wrinkles: R53 first.middleinitial.last is the frequent form (middle-initial dependence); R49 mixes firstinitial+last with firstname+last and middle-initial variants; R55 appends a numeric suffix on collisions.
- Aggregators conflict with real samples again: R45 (Prospeo firstinitial.last vs real first.last), R48 (RocketReach/ContactOut vs Prospeo), R51 (SignalHire lastName_firstName outlier), R54 (Prospeo firstinitial.last vs real first.last). Trust real in-session samples over aggregator percentages.
- Functional-only / no personal sample: R48 (USVI).
- Officeholder changes/flags for Phase 3: R45 (Commissioner Bill Even; Joe Fiala now Deputy — confirmed change April 2025). Plus CEO/Director verify for R46, R47 (Cruz), R48 (Latham — likely stale), R49 (Moss/Rosander), R50 (Farrell vs stale Moulton), R51 (El Koubi vs stale Anderson/Vuori), R52 (Clifthorne interim), R53, R54 (Miller; ContactOut CEO label wrong), R55 (Dorrell).

---

# PHASE 2 — DEFAULT ORG EMAIL

## Phase 2 evidence (R01–R11)
Scoring: org_email_confidence = base + recency (no officeholder factor). base T1=90 / T3=60. Live official contact pages returned today scored at recency +0 (treated as current) unless a clearly old date showed.

## R01 — Alabama — contact@madeinalabama.com — VALIDATED (T1) — 90
- Source: official Made in Alabama Contact page https://www.madeinalabama.com/contact/. Quote: "Email contact@madeinalabama.com".
- Math: T1 base 90 + recency 0 = 90. Input guess contact@madeinalabama.com is correct. Also shown on the official Department of Commerce Facebook.

## R02 — Alaska — dcced.commissioner@alaska.gov — VALIDATED (T1) — 90
- Source: official DCCED Contact Us page https://www.commerce.alaska.gov/web/ContactUs.aspx. Quote: "Email: dcced.commissioner@alaska.gov".
- Math: T1 base 90 + recency 0 = 90. The department publishes a directory of division emails rather than one info@; the Commissioner Office address is the top-level department contact. Input guess AlaskaDevelopment@alaska.gov was NOT found on any official page. ALT division contacts: dbsc@alaska.gov, ced.abo.general@alaska.gov.

## R03 — American Samoa — info@doc.as — VALIDATED (T1) — 90
- Source: official ASDOC Application Center page https://www.doc.as.gov/application-center. Quote: "PLEASE CALL 633-5155 FOR MORE INFORMATION OR EMAIL US AT INFO@DOC.AS.".
- Math: T1 base 90 + recency 0 = 90. Input guess info@doc.as is correct. Note the general inbox uses @doc.as while individual staff use @doc.as.gov. ALT: americansamoastatistics@doc.as.gov (Statistics Division).

## R04 — Arizona — (none) — UNVERIFIED — 5
- Source checked: official ACA Get-in-Touch / Contact Us pages https://www.azcommerce.com/get-in-touch/ and /about-us/contact-us/.
- Finding: no general public email published; contact is via a web form plus individual "Email [Name]" buttons. Input guess events@azcommerce.com was NOT confirmed on a T1 page. Math: nothing found = 5. Retry Phase 5.

## R05 — Arkansas — info@arkansasedc.com — INFERRED (T3) — 65
- Source: JAN organization listing https://askjan.org/organizations/Arkansas-Economic-Development-Commission.cfm. Quote: "Email: info@arkansasedc.com".
- Corroboration: the official AEDC Facebook lists info@arkansasedc.com as the page contact; multiple directories (GrantForward, exportarkansas) agree; Phase 1 decoded info@arkansasedc.com from the official arkansasedc.com media-inquiries link. Math: T3 base 60 + recency 5 (current) = 65. Could upgrade to VALIDATED with a direct official-site fetch in Phase 5.

## R06 — California — (none) — UNVERIFIED — 5
- Source checked: official GO-Biz Contact Us page https://business.ca.gov/about/contact-us/.
- Finding: no general public email; contact is by phone (1-877-345-4633) and a web form. Only functional program inboxes exist (hydrogen@, gobiz.hr@gobiz.ca.gov). Math: nothing found = 5. Retry Phase 5.

## R07 — Colorado — oedit.info@state.co.us — VALIDATED (T1) — 90
- Source: official OEDIT Reports page https://oedit.colorado.gov/about/oedit-reports. Quote: "please email oedit.info@state.co.us or call the office at 303-892-3840".
- Corroboration: the same inbox is repeated in the footer of every OEDIT staff bio page (e.g., /karen-crowe, /gina-atencio) and on choosecolorado.com/contact-us and the official OEDIT Facebook. Math: T1 base 90 + recency 0 = 90. Input guess oedit.info@state.co.us is correct.

## R08 — Connecticut — DECD@ct.gov — INFERRED (T3) — 60
- Source: JAN organization listing https://askjan.org/organizations/Connecticut-Department-of-Economic-and-Community-Development.cfm. Quote: "Email: DECD@ct.gov".
- Note: matches the official portal.ct.gov/DECD Contact page found in Phase 1; not re-fetched at T1 this session. Math: T3 base 60 + recency 0 = 60. Input guess decd@ct.gov is correct. Could upgrade to VALIDATED with an official-page fetch in Phase 5.

## R09 — Delaware — business@delaware.gov — VALIDATED (T1) — 90
- Source: official business.delaware.gov News & Publications page https://business.delaware.gov/news-publications. Quote: "business@delaware.gov".
- Corroboration: the same general inbox appears in the standard footer across many official business.delaware.gov pages and on the official Division of Small Business LinkedIn. Math: T1 base 90 + recency 0 = 90. Input guess business@delaware.gov is correct.

## R10 — Florida — CustomerInfoCenter@commerce.fl.gov — VALIDATED (T1) — 90
- Source: official Employ Florida Help Desk Contact page https://www.employflorida.com/vosnet/ContactUs.aspx. Quote: "System Contact Email: CustomerInfoCenter@commerce.fl.gov".
- Note: Employ Florida is the official state workforce system operated by FloridaCommerce. Math: T1 base 90 + recency 0 = 90. Input guess CustomerInfoCenter@commerce.fl.gov is correct. ALT functional: OIG@, media@commerce.fl.gov. FL public-records notice limits publication of personal staff emails.

## R11 — Georgia — (none) — UNVERIFIED — 5
- Source checked: official georgia.org About Us page https://georgia.org/about-us (directs to "contact the Georgia Department of Economic Development or call 404.962.4000").
- Finding: no general email surfaced verbatim on an official page this session; the georgia.org and georgia.gov contact snippets masked the address. Input guess econdev@georgia.org NOT confirmed this session (Phase 1 noted georgia.org/media-contacts). Math: nothing found = 5. Retry Phase 5 (fetch georgia.gov/contacts/department-economic-development-contact).

## Phase 2 batch summary (R01–R11)
- VALIDATED (T1, 90): R01, R02, R03, R07, R09, R10 — six general/department inboxes confirmed on official pages with verbatim quotes.
- INFERRED (T3): R05 (65), R08 (60) — confirmed via official social/third-party directories this session; official-site fetch can upgrade them in Phase 5.
- UNVERIFIED (5): R04 (AZ), R06 (CA), R11 (GA) — no general public email published; AZ and CA use web forms/phone, GA masked the address in snippets. Flag for Phase 5.
- Input-guess accuracy: correct for R01, R03, R07, R09, R10; input guess unconfirmed/likely wrong for R02 (AlaskaDevelopment@ not found), R04 (events@ not confirmed), R11 (econdev@ not surfaced).
- org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] this batch = 6/2/3/0/0.

## R12 — Guam — social@investguam.com — INFERRED (T3) — 65
- Source: official GEDA Facebook page https://www.facebook.com/GuamEconomicDevelopmentAuthority/. Quote: "social@investguam.com" (listed as the Government-organization page contact).
- Corroboration: Crunchbase lists the same contact email. Official investguam.com Contact/About pages show phone 671-647-4332 only; input guess info@investguam.com NOT surfaced verbatim this session. Functional inboxes: help@, smallbusiness@, procurement@, qcgrants@investguam.com. Math: T3 base 60 + recency 5 (page current) = 65.

## R13 — Hawaii — director@dbedt.hawaii.gov — VALIDATED (T1) — 90
- Source: official State of Hawaii agency directory https://portal.ehawaii.gov/government/departments-and-agencies/. Quote: "Email: director@dbedt.hawaii.gov".
- Note: department general inbox; the DBEDT own Contact page lists phone 808-586-2355 only. Input guess dbedt@hawaii.gov NOT found. Math: T1 base 90 + recency 0 = 90.

## R14 — Idaho — info@commerce.idaho.gov — VALIDATED (T1) — 90
- Source: official Idaho Commerce FAQ page https://commerce.idaho.gov/faqs/. Quote: "Contact us at info@commerce.idaho.gov, or fill out the form at the bottom of this page".
- Math: T1 base 90 + recency 0 = 90. Input guess info@commerce.idaho.gov is correct.

## R15 — Illinois — (none) — UNVERIFIED — 5
- Source checked: official DCEO Contact Us page https://dceo.illinois.gov/oe3/contact-us.html (web form plus named program-staff emails such as Diana.Alfaro@illinois.gov; Business Information Center phone 800.252.2923).
- Finding: no general public inbox published; input guess dceo.webmail@illinois.gov NOT surfaced this session. Program inbox ceo.EECProgram@illinois.gov exists. Math: nothing found = 5. Retry Phase 5.

## R16 — Indiana — iedc@iedc.in.gov — VALIDATED (T1) — 90
- Source: official IEDC Contact page footer https://iedc.in.gov/contact. Quote: "iedc@iedc.in.gov".
- Corroboration: official IEDC Facebook (Government organization, iedc@iedc.in.gov) and the JAN directory ("Email: iedc@iedc.in.gov"). Input guess info@iedc.in.gov differs from the published general inbox iedc@iedc.in.gov. Math: T1 base 90 + recency 0 = 90.

## R17 — Iowa — info@iowaeda.com — VALIDATED (T1) — 90
- Source: official Iowa EDA Contact Us page https://www.iowaeda.com/contact-us/. Quote: "Iowa Economic Development Authority 1963 Bell Avenue, Suite 200 Des Moines, Iowa 50315 USA 515.348.6200 info@iowaeda.com".
- Note: functional director@, communications@, boardinfo@, traveliowa@iowaeda.com. Math: T1 base 90 + recency 0 = 90. Input guess info@iowaeda.com is correct.

## R18 — Kansas — (none) — UNVERIFIED — 5
- Source checked: official Kansas Commerce site https://www.kansascommerce.gov/ (main department contact is phone 785-296-3481).
- Finding: no general public inbox; input guess info@kansascommerce.com NOT found. Official Kansas Commerce Facebook lists a media inbox commercenews@ks.gov; program inbox ruralkanprosper@ks.gov. Math: nothing found = 5. Retry Phase 5.

## R19 — Kentucky — econdev@ky.gov — VALIDATED (T1) — 90
- Source: official Kentucky CED Contact page https://newkentuckyhome.ky.gov/Home/ContactUs. Quote: "To contact the Cabinet by email, send inquiries to Quick Contact Or econdev@ky.gov".
- Note: open records CEDOpenRecords@ky.gov. Math: T1 base 90 + recency 0 = 90. Input guess econdev@ky.gov is correct.

## R20 — Louisiana — LED@la.gov — VALIDATED (T1) — 90
- Source: official LED Leadership Staff page https://www.opportunitylouisiana.gov/about-led/leadership-staff. Quote: "Request LED leadership to speak at your event by emailing LED@la.gov".
- Corroboration: the same general inbox appears on the official LED Need-to-Know page. Functional LEDPublicRecords@la.gov. Math: T1 base 90 + recency 0 = 90. Input guess LED@la.gov is correct.

## R21 — Maine — business.answers@maine.gov — VALIDATED (T1) — 90
- Source: official Maine DECD Connections page https://www.maine.gov/decd/business-development/resource-compass/connections. Quote: "Not finding what you are looking for? Email us at business.answers@maine.gov".
- Corroboration: the official Maine Business Answers page (maine.gov/businessanswers) lists the same inbox. Input guess biz.development@maine.gov NOT found; the official DECD general inbox is business.answers@maine.gov. Math: T1 base 90 + recency 0 = 90.

## R22 — Maryland — (none) — UNVERIFIED — 5
- Source checked: official Maryland Commerce site https://commerce.maryland.gov/ (main contact phone 410-767-6300 / 888-246-6736).
- Finding: no general public inbox surfaced on official pages; input guess secretary.commerce@maryland.gov NOT found. The JAN directory lists a comms inbox communications.commerce@maryland.gov; the MD PIA Manual lists PIA officer karen.glennhood@maryland.gov. Math: nothing found = 5. Retry Phase 5.

## Phase 2 batch summary (R12–R22)
- VALIDATED (T1, 90): R13, R14, R16, R17, R19, R20, R21 — seven general/department inboxes confirmed on official pages with verbatim quotes.
- INFERRED (T3): R12 (65) — confirmed via the official GEDA Facebook this session; official-site fetch can upgrade it in Phase 5.
- UNVERIFIED (5): R15 (IL), R18 (KS), R22 (MD) — no general public inbox published; web form/phone only; input guesses not found. Flag for Phase 5.
- Input-guess accuracy: correct for R14, R17, R19, R20; input guess wrong/unconfirmed for R12 (info@ not surfaced), R13 (dbedt@hawaii.gov not found; actual director@dbedt.hawaii.gov), R16 (info@ differs from iedc@), R21 (biz.development@ not found; actual business.answers@), and R15/R18/R22 (not found).
- org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] this batch = 7/1/3/0/0.

## R23 — Massachusetts — (none) — UNVERIFIED — 5
- Source checked: official EOED page https://www.mass.gov/orgs/executive-office-of-economic-development (Contact Us is a web form).
- Finding: general intake routes through the Business Front Door web form (mass.gov/bfd); the only published emails are press contact margaret.m.quackenbush@mass.gov and records office HED.RAO@massmail.state.ma.us. No general public inbox. Math: nothing found = 5. Retry Phase 5.

## R24 — Michigan — (none) — UNVERIFIED — 5
- Source checked: official MEDC Contact page https://www.michiganbusiness.org/about-medc/contact-medc/ (web form).
- Finding: general contact is phone 1.888.522.0103 via a web form; no general public email inbox. Functional FOIA medcfoia@michigan.org; press emersond1@michigan.org. Math: nothing found = 5. Retry Phase 5.

## R25 — Minnesota — DEED.CustomerService@state.mn.us — INFERRED (T3) — 65
- Source: official DEED Facebook https://www.facebook.com/mndeed/ (current). Quote: "DEED.CustomerService@state.mn.us".
- Corroboration: UMN MBBNet partner directory lists the same inbox. Input guess deed.customerservice@state.mn.us is correct. The official mn.gov/deed Contact page references email but did not surface the address verbatim this session. Math: T3 base 60 + recency 5 = 65. Upgrade to T1 in Phase 5 via the official Contact page.

## R26 — Mississippi — (none) — UNVERIFIED — 5
- Source checked: official MDA site https://mississippi.org/.
- Finding: no general public inbox surfaced verbatim on official pages this session; input guess info@mississippi.org NOT confirmed. Program inbox msgrid@mississippi.org (Grid Resilience, on the official MDA RFA PDF); MDA-ENRD phone 601-359-3449. Math: nothing found = 5. Retry Phase 5.

## R27 — Missouri — ecodev@ded.mo.gov — VALIDATED (T1) — 90
- Source: official DED Contact page https://ded.mo.gov/advanced-manufacturing/contact. Quote: "Missouri Department of Economic Development Phone: 573-751-4962 Email: ecodev@ded.mo.gov".
- Note: input guess ecodev@ded.mo.gov is correct. Math: T1 base 90 + recency 0 = 90.

## R28 — Montana — (none) — UNVERIFIED — 5
- Source checked: official Montana Commerce Leadership page https://commerce.mt.gov/about/leadership and site footer (Contact Us web form + phone 406-841-2700).
- Finding: no general public email inbox; only personal staff emails (first.last@mt.gov) and a public-records inbox publicrecords@mt.gov. Math: nothing found = 5. Retry Phase 5.

## R29 — Nebraska — (none) — UNVERIFIED — 5
- Source checked: official DED Contact page https://opportunity.nebraska.gov/contact/ (main contact phone 800-426-6505 / 402-471-3111).
- Finding: no general public inbox; input guess opportunity@nebraska.gov NOT found. Program inbox ded.imagine@nebraska.gov (ImagiNE Act, on the official imagine.nebraska.gov apply page). Math: nothing found = 5. Retry Phase 5.

## R30 — Nevada — goed@goed.nv.gov — VALIDATED (T1) — 90
- Source: official GOED Contact page https://goed.nv.gov/contact/. Quote: "808 West Nye Lane Carson City, NV 89703 (775) 687-9900 goed@goed.nv.gov".
- Note: the same inbox is listed for both the Carson City and Las Vegas offices. Resolves the Phase 1 domain conflict: goed.nv.gov is the operating domain; diversifynevada.com is a marketing alias. Input guess info@diversifynevada.com NOT used. Math: T1 base 90 + recency 0 = 90.

## R31 — New Hampshire — info@nheconomy.com — INFERRED (T3) — 60
- Source: JAN organization directory https://askjan.org/organizations/New-Hampshire-Department-of-Business-and-Economic-Affairs.cfm. Quote: "Email: info@nheconomy.com".
- Corroboration: SignalHire lists the same general inbox. Not surfaced verbatim on an official nheconomy.com/dbea.nh.gov page this session (official Meet the Staff lists names/phones only). OFFICEHOLDER (Phase 3): Commissioner Lucy Lange (Taylor Caswell departed). Math: T3 base 60 + recency 0 = 60. Upgrade to T1 in Phase 5.

## R32 — New Jersey — CustomerCare@njeda.com — VALIDATED (T1) — 90
- Source: official NJEDA About page https://www.njeda.gov/about/. Quote: "36 West State Street, Trenton, NJ 08625 Phone: (609) 858-6700 E-mail: CustomerCare@njeda.com".
- Note: the same inbox is listed for both the Trenton and Newark offices. ALT functional oprae-mail@njeda.gov (OPRA public records). Email domain splits njeda.gov/njeda.com. Math: T1 base 90 + recency 0 = 90.

## R33 — New Mexico — info@edd.nm.gov — VALIDATED (T1) — 90
- Source: official EDD Contact Us page https://www.edd.newmexico.gov/contact-us/. Quote: "Main number: (505) 827-0300 Fax: (505) 827-0328 Email: info@edd.nm.gov".
- Note: input guess info@edd.nm.gov is correct. ALT edd.info@edd.nm.gov (official EDD Facebook). Email domain edd.nm.gov differs from website edd.newmexico.gov. Math: T1 base 90 + recency 0 = 90.

## Phase 2 batch summary (R23–R33)
- VALIDATED (T1, 90): R27 (MO ecodev@ded.mo.gov), R30 (NV goed@goed.nv.gov), R32 (NJ CustomerCare@njeda.com), R33 (NM info@edd.nm.gov) — four general inboxes confirmed on official pages with verbatim quotes.
- INFERRED (T3): R25 (MN, 65, official DEED Facebook + UMN directory), R31 (NH, 60, JAN + SignalHire) — both upgradeable to T1 in Phase 5.
- UNVERIFIED (5): R23 (MA), R24 (MI), R26 (MS), R28 (MT), R29 (NE) — no general public inbox published; web form/phone only; input guesses not found or not confirmed. Flag for Phase 5.
- Input-guess accuracy: correct for R27, R33; resolved differently for R30 (input info@diversifynevada.com not used; actual goed@goed.nv.gov), R32 (CustomerCare@njeda.com is the general inbox); unconfirmed for R25 (input correct but only T3 this session), R26/R29 (not found), R23/R24/R28 (no inbox); R31 input info@nheconomy.com corroborated only by third parties.
- org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] this batch = 4/2/5/0/0.

## R34 — New York — ESD@esd.ny.gov — VALIDATED (T2) — 87
- Source: official ESD board-meeting media advisory (current Jan 2026) https://esd.ny.gov/sites/default/files/media/document/ESD-Directors-Meeting-11526.pdf. Quote: "Members of the public may submit comments on the Agenda items in writing to ESD@esd.ny.gov".
- Note: the ESD Contact Us page routes general inquiries via office phones and Email Us web forms; ESD@esd.ny.gov is the general-purpose inbox published verbatim across many official board-meeting advisories. PressOffice@ is media-only; NYEZC@/ESNMCBDMTG@ are subsidiary/program-specific. Math: T2 base 82 + recency 5 (current) = 87.

## R35 — North Carolina — (none) — UNVERIFIED — 5
- Source checked: official EDPNC site https://edpnc.com/find-a-site/site-development-initiatives/.
- Finding: no general public inbox surfaced verbatim; main contact is the Business Concierge phone 1-800-228-8443 / 919-447-7777. Input guess client.services@edpnc.com NOT found; functional cir@edpnc.com (research). Math: nothing found = 5. Retry Phase 5.

## R36 — North Dakota — (none) — UNVERIFIED — 5
- Source checked: official ND Commerce Contact page https://www.commerce.nd.gov/contact.
- Finding: general questions route via a web form (main phone 701-328-5300); no general public email inbox. Input guess ndcommerce@nd.gov NOT confirmed this session. Math: nothing found = 5. Retry Phase 5.

## R37 — Northern Mariana Islands — info@commerce.gov.mp — VALIDATED (T1) — 90
- Source: official CNMI Commerce site https://www.commerce.gov.mp/. Quote: "For questions or comments you may email us at info@commerce.gov.mp".
- Corroboration: same inbox on the official About Us and Secretary of Commerce pages. CONFIRMS the Phase-1 domain correction: email/website domain is commerce.gov.mp, not the input commerce.cnmi.gov. Role-based registrar.reyes@commerce.gov.mp. Math: T1 base 90 + recency 0 = 90.

## R38 — Ohio — (none) — UNVERIFIED — 5
- Source checked: official Ohio APEX / govcontracts contact page https://find.govcontracts.ohio.gov/contact/ (an Ohio Department of Development program).
- Finding: no general public inbox surfaced verbatim on official development.ohio.gov pages; main contact phone 1-800-848-1300; personal staff are first.last@development.ohio.gov. Math: nothing found = 5. Retry Phase 5.

## R39 — Oklahoma — hello@okcommerce.gov — VALIDATED (T1) — 80
- Source: official okcommerce.gov accessibility statement https://www.okcommerce.gov/about-us/accessibility-statement/. Quote: "please email hello@okcommerce.gov or call (405) 815-6552".
- Note: input guess info@okcommerce.gov differs; the general inbox is hello@okcommerce.gov. The verbatim source page is dated 2022. OFFICEHOLDER (Phase 3): Secretary Deborah Moorad now leads Commerce per the okcommerce.gov Our Team page (Jan 2026), superseding Phase-1 Kouplen/Kisling. Math: T1 base 90 + recency -10 (25-48mo source) = 80. Re-confirm on a current contact page in Phase 5.

## R40 — Oregon — biz.info@state.or.us — INFERRED (T3) — 65
- Source: official Business Oregon Facebook https://www.facebook.com/BusinessOregon/ (current). Quote: "biz.info@state.or.us".
- Note: the official oregon.gov/biz Contact page did not surface an email verbatim this session. Input guess business.oregon@oregon.gov NOT confirmed. Phase-1 functional Business.OREGON_INFO@biz.oregon.gov; both state.or.us and biz.oregon.gov email domains appear. Math: T3 base 60 + recency 5 (current) = 65. Upgrade to T1 in Phase 5.

## R41 — Pennsylvania — (none) — UNVERIFIED — 5
- Source checked: official DCED Community Planning page https://dced.pa.gov/housing-and-development/community-planning/ (and a PA.gov resource page citing DCED contacts).
- Finding: no general public email inbox; DCED general inquiries are by phone 866-466-3972 (PA Business One-Stop Shop 833-722-6778). Personal staff are firstinitial+last@pa.gov; functional RA-DCEDHousingPlan@pa.gov. Math: nothing found = 5. Retry Phase 5.

## R42 — Puerto Rico — info@ddec.pr.gov — VALIDATED (T1) — 90
- Source: official DDEC Comercial Mission portal (ddec.pr.gov domain) https://misioncomercial.ddec.pr.gov/Home/Login. Quote: "787-765-2900 info@ddec.pr.gov" (page footer).
- Note: input guess info@ddec.pr.gov correct; upgrades the Phase-1 UNVERIFIED convention. Program inbox promoexport@ddec.pr.gov (trade/export). OFFICEHOLDER confirmed current Secretary Sebastian Negron Reichard (Phase 3). Math: T1 base 90 + recency 0 = 90.

## R43 — Rhode Island — info@commerceri.com — VALIDATED (T1) — 90
- Source: official RI Commerce Contact Us page https://commerceri.com/contact-us/. Quote: "315 Iron Horse Way, Suite 101, Providence, RI 02908 Phone: 401-278-9100 Email: info@commerceri.com".
- Corroboration: same inbox on the official commerceri.com accessibility page. Input guess info@commerceri.com correct; program inbox MainStreet@commerceri.com. (Row structure was corrected from 38 to 39 columns this write.) Math: T1 base 90 + recency 0 = 90.

## R44 — South Carolina — LocateSC@sccommerce.com — VALIDATED (T1) — 90
- Source: official SC Commerce LocateSC contact page https://locatesc.sccommerce.com/contact.html. Quote: "1201 Main Street, Suite 1600 Columbia SC 29201 Phone: +1 (803) 737-0400 Email: LocateSC@sccommerce.com".
- Note: LocateSC@sccommerce.com is the agency primary public business-contact inbox. Input guess info@sccommerce.com NOT surfaced verbatim this session; small-business inbox SmallBizSupport@sccommerce.com. OFFICEHOLDER (Phase 3): verify current Secretary (input leader Harry Lightsey may be stale). (Row structure was corrected from 38 to 39 columns this write.) Math: T1 base 90 + recency 0 = 90.

## Phase 2 batch summary (R34–R44)
- VALIDATED: R34 (NY ESD@esd.ny.gov, T2 87), R37 (CNMI info@commerce.gov.mp, T1 90), R39 (OK hello@okcommerce.gov, T1 80 - 2022 source), R42 (PR info@ddec.pr.gov, T1 90), R43 (RI info@commerceri.com, T1 90), R44 (SC LocateSC@sccommerce.com, T1 90) — six confirmed on official pages with verbatim quotes.
- INFERRED (T3): R40 (OR biz.info@state.or.us, 65) — official Business Oregon Facebook; upgradeable to T1 in Phase 5.
- UNVERIFIED (5): R35 (NC), R36 (ND), R38 (OH), R41 (PA) — no general public inbox published; web form/phone only; input guesses not found. Flag for Phase 5.
- Input-guess accuracy: correct for R42, R43; resolved differently for R37 (domain corrected to commerce.gov.mp), R39 (hello@ not the input info@), R44 (LocateSC@, input info@ not surfaced); unconfirmed for R35/R36/R38/R41 (not found); R34 ESD@ and R40 biz.info@ differ from any input guess.
- STRUCTURAL FIX: R43 and R44 were written in Phase 1 with 38 columns (one empty field short, open_issues in col36). Both rebuilt to the correct 39-column schema this batch. Whole-file check now passes: all 55 rows = 39 columns.
- org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] this batch = 6/1/4/0/0.

## R45 — South Dakota — goedinfo@state.sd.us — INFERRED (T3) — 60
- Source: JAN directory https://askjan.org/concerns/Economic-Development-Business-Office.cfm. Quote: "711 E. Wells Avenue Pierre, SD 57501 Toll Free: (800) 872-6190 Email: goedinfo@state.sd.us".
- Note: Phase 1 found the same address on the official sdgoed.com Contact Us page; this session only the JAN third-party directory surfaced it verbatim, so INFERRED T3 (upgrade to T1 in Phase 5). Email domain state.sd.us differs from website sdgoed.com. OFFICEHOLDER (Phase 3): Commissioner Bill Even (appointed Apr 2025); Joe Fiala now Deputy. Math: T3 base 60 + recency 0 = 60.

## R46 — Tennessee — ECD.Communications.Office@tn.gov — VALIDATED (T1) — 90
- Source: official TNECD Contact Us page https://tnecd.com/about/contact/. Quote: "(615) 741-1888 ECD.Communications.Office@tn.gov".
- Corroboration: current TN SOS rules 0500 publication lists the same address as the department contact. TNECD publishes no info@ general inbox; this Communications Office inbox is the published public contact. Personal staff are first.last@tn.gov; email domain tn.gov differs from website tnecd.com. Math: T1 base 90 + recency 0 (corroborated current) = 90.

## R47 — Texas — business@gov.texas.gov — INFERRED (T3) — 65
- Source: official Texas Economic Development and Tourism Facebook https://www.facebook.com/TexasEconDev/ (current). Quote: "business@gov.texas.gov".
- Note: the official gov.texas.gov/business Contact Us page routes via a web form and did not surface an email verbatim this session. Functional TexasProduct.Fund@gov.texas.gov; EDT sits within the Office of the Governor. Upgrade to T1 in Phase 5. Math: T3 base 60 + recency 5 (current) = 65.

## R48 — U.S. Virgin Islands — info@usvieda.org — VALIDATED (T1) — 95
- Source: official USVIEDA news post https://usvieda.org/2026/01/20/virgin-islands-economic-development-authority-governing-board-decision-meeting/ (Jan 2026). Quote: "For more information, please send an email to info@usvieda.org".
- Corroboration: same inbox on the Dec 2025 official USVIEDA news post. Input guess info@usvieda.org correct; media/PR inbox marketing@usvieda.org. OFFICEHOLDER (Phase 3): older releases name CEO Kamal Latham - verify current (input Wayne L. Biggs Jr.). Math: T1 base 90 + recency 5 (Jan 2026, current) = 95.

## R49 — Utah — business@utah.gov — VALIDATED (T1) — 95
- Source: official GOEO Contact page https://business.utah.gov/contact/ (Mar 2026). Quote: "We are here to help EMAIL business@utah.gov PHONE 801-538-8680 ADDRESS 60 East South Temple, Suite 300 Salt Lake City, Utah 84111-1041".
- Corroboration: same inbox on the official Boards page. Input guess correct; grants econgrants@utah.gov; media Marcus Hardy; GRAMA officer Patrick Fitzgibbon. OFFICEHOLDER (Phase 3): ED/Commissioner Jefferson Moss, Deputy Tara Rosander (input leader Ryan Starks - verify). Math: T1 base 90 + recency 5 (Mar 2026, current) = 95.

## R50 — Vermont — ACCD.DEDInfo@vermont.gov — VALIDATED (T1) — 90
- Source: official ACCD Business Resources page https://accd.vermont.gov/economic-development/business-resources. Quote: "The Department of Economic Development is here to help you find the right tools for your business. Contact us at ACCD.DEDInfo@vermont.gov".
- Note: this is the general Department of Economic Development inbox (best default for an economic-development EDC). Program inbox ACCD.APEXinfo@vermont.gov (APEX); the ACCD Contact Us page lists personal staff (first.last@vermont.gov). OFFICEHOLDER (Phase 3): input Secretary Lindsay Kurrle - verify (Phase 1 found Commissioner of DED Alex Farrell). Math: T1 base 90 + recency 0 = 90.

## R51 — Virginia — info@vedp.org — VALIDATED (T1) — 90
- Source: official VEDP privacy policy https://www.vedp.org/privacy-policy. Quote: "please contact VEDP by emailing info [at] vedp.org (info[at]vedp[dot]org)" (anti-spam obfuscation; de-obfuscated address is info@vedp.org).
- Corroboration: JAN directory lists the plain address info@vedp.org. Input guess info@vedp.org correct; personal staff firstinitial+last@vedp.org. OFFICEHOLDER (Phase 3): President and CEO Jason El Koubi confirmed on the official VEDP Staff Directory. Math: T1 base 90 + recency 0 = 90.

## R52 — Washington — ChooseWashington@commerce.wa.gov — VALIDATED (T1) — 70
- Source: official WA Commerce OEDC Contact Us page https://choosewashingtonstate.com/contact-us/. Quote: "Phone: 206.256.6100 Fax: 206.256.6158 eMail: ChooseWashington@commerce.wa.gov".
- Note: ChooseWashington@commerce.wa.gov is the public OEDC business inbox, but the verbatim source page is dated 2012 (recency -20) - re-confirm in Phase 5. The current official commerce.wa.gov Staff Resources page lists ComCustServ@commerce.wa.gov (Information Services) and the main phone is 360-725-4000. Input guess info@commerce.wa.gov NOT surfaced. OFFICEHOLDER (Phase 3): interim Director Sarah Clifthorne (input leader Mike Fong - verify). Math: T1 base 90 + recency -20 (49+mo source) = 70.

## R53 — West Virginia — (none) — UNVERIFIED — 5
- Source checked: official WV Dept of Economic Development regional-rep map https://westvirginia.gov/connect-with-us/wv-economic-development-regional-representative-map/.
- Finding: no general public inbox surfaced verbatim on the official site this session; main contact phone (304) 558-2234 / (800) 982-3386; personal staff first.middleinitial.last@wv.gov; webmaster commercewebmaster@wv.gov. Input guess quotes@wv.gov NOT confirmed; askme@wv.gov is SBDC-specific (third-party 2017 source); WVOEInfo@wv.gov is the Office of Energy inbox. Math: nothing found = 5. Retry Phase 5.

## R54 — Wisconsin — (none) — UNVERIFIED — 5
- Source checked: official WEDC Contact Us page https://wedc.org/contact-us/.
- Finding: the page routes via a web form, a media contact (david.callender@wedc.org), and phone (855) 469-3247 / 608-210-6700; no general info@/contact@ inbox surfaced verbatim this session. Functional events@wedc.org and program inbox investmentfund@wedc.org. OFFICEHOLDER confirmed Secretary and CEO John W. Miller (Phase 3). Math: nothing found = 5. Retry Phase 5.

## R55 — Wyoming — info.wbc@wyo.gov — VALIDATED (T1) — 90
- Source: official WBC About Us page https://w.wyomingbusiness.org/about. Quote: "Wyoming Business Council 214 West 15th St. Cheyenne, WY 82002 307.777.2800 info.wbc@wyo.gov".
- Corroboration: same address on the official WBC Home page. Email domain is wyo.gov, NOT the website wyomingbusiness.org. Input guess wbc.info@wyo.gov has the local-part reversed (actual is info.wbc@). OFFICEHOLDER confirmed CEO Josh Dorrell (Phase 3). NOTE: WBC faces a Jan 2026 legislative proposal to dismantle the agency - monitor. Math: T1 base 90 + recency 0 = 90.

## Phase 2 batch summary (R45–R55)
- VALIDATED: R46 (TN ECD.Communications.Office@tn.gov, T1 90), R48 (USVI info@usvieda.org, T1 95), R49 (UT business@utah.gov, T1 95), R50 (VT ACCD.DEDInfo@vermont.gov, T1 90), R51 (VA info@vedp.org, T1 90), R52 (WA ChooseWashington@commerce.wa.gov, T1 70 - 2012 source), R55 (WY info.wbc@wyo.gov, T1 90) — seven confirmed on official pages with verbatim quotes.
- INFERRED (T3): R45 (SD goedinfo@state.sd.us, 60, JAN directory; official sdgoed.com page in Phase 1), R47 (TX business@gov.texas.gov, 65, official Texas EconDev Facebook) — both upgradeable to T1 in Phase 5.
- UNVERIFIED (5): R53 (WV), R54 (WI) — no general public inbox published; web form/phone only; input guesses not found. Flag for Phase 5.
- Input-guess accuracy: correct for R48, R49, R51 (info@/business@); resolved differently for R45 (goedinfo@ not input), R46 (ECD.Communications.Office@), R47 (business@ via FB), R50 (ACCD.DEDInfo@), R52 (ChooseWashington@, input info@ not surfaced), R55 (info.wbc@, input wbc.info@ reversed); unconfirmed for R53/R54 (not found).
- org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] this batch = 7/2/2/0/0.

## PHASE 2 COMPLETE — all 55 records (R01–R55), cols 20–26 filled
- Phase 2 totals across all 55: org[VALIDATED/INFERRED/UNVERIFIED/CONFLICT/DEAD] = 30/8/17/0/0.
- By batch: B1 (R01–R11) 6/2/3 - B2 (R12–R22) 7/1/3 - B3 (R23–R33) 4/2/5 - B4 (R34–R44) 6/1/4 - B5 (R45–R55) 7/2/2.
- Phase 5 org-email upgrade targets (INFERRED-T3 or recency-discounted, push to T1 where possible): R05, R08, R12, R25, R31, R40, R45, R47 (T3); R39 (2022 source, 80), R52 (2012 source, 70).
