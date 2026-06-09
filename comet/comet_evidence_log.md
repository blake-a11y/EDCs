# COMET EVIDENCE LOG — EDC Email Validation
Show-your-math proof. Appended each phase. URLs are pages actually opened during research.

---

## PHASE 1 — Domain + Naming Convention

### R01 — Alabama — The Alabama Development Fund
- Canonical domain: `commerce.alabama.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.madeinalabama.com/resources/staff-directory/
- Sample 1: `ellen.mcnair@commerce.alabama.gov` — https://www.madeinalabama.com/resources/staff-directory/
- Sample 2: `erika.mckay@commerce.alabama.gov` — https://www.madeinalabama.com/resources/staff-directory/
- Pattern: first.last | convention_confidence: 40
- Math: The staff directory explicitly lists dozens of emails following the first.last@commerce.alabama.gov pattern. Samples found include ellen.mcnair@commerce.alabama.gov and erika.mckay@commerce.alabama.gov. Some variations with middle initials exist (e.g., margaretm.henderson) likely for differentiation, but the primary convention is first.last.

### R02 — Alaska — The Alaska Department of Commerce, Community, and Economic Development
- Canonical domain: `alaska.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.alaska.gov/commlist.html
- Sample 1: `julie.sande@alaska.gov` — https://www.alaska.gov/commlist.html
- Sample 2: `hannah.lager@alaska.gov` — https://omb.alaska.gov/ombfiles/25_budget/DCCED/Proposed/1_dept8.pdf
- Pattern: first.last | convention_confidence: 90
- Math: julie.sande@alaska.gov + hannah.lager@alaska.gov => first.last. Multiple samples confirmed across official state lists and budget documents.

### R03 — American Samoa — The American Samoa Department of Commerce
- Canonical domain: `doc.as.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.doc.as.gov/about
- Sample 1: `uili.leauanae@doc.as.gov` — https://www.doc.as.gov/about
- Sample 2: `mine.timoteo@doc.as.gov` — https://www.doc.as.gov/about
- Pattern: first.last | convention_confidence: 75
- Math: The staff directory on the About page lists 10 staff members, all using the first.last@doc.as.gov pattern. For example, Uili Leauanae is uili.leauanae@doc.as.gov and Mine Timoteo is mine.timoteo@doc.as.gov. Some use preferred names (e.g., Lina Petaia for Aliimuamua Magdalene 'Lina' Petaia-Suisala).

### R04 — Arizona — The Arizona Commerce Authority
- Canonical domain: `azcommerce.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.azcommerce.com/about-us/executive-management-team/
- Sample 1: `KenB@azcommerce.com` — https://www.azcommerce.com/about-us/executive-management-team/
- Sample 2: `ShawnN@azcommerce.com` — https://www.azcommerce.com/about-us/executive-management-team/
- Pattern: CATCH_ALL_UNKNOWN | convention_confidence: 25
- Math: Based on the staff emails found on the executive team page, the naming convention follows the 'flast' (first initial + last name) pattern. For example, Ken Burns is KenB@azcommerce.com and Shawn Neidorf is ShawnN@azcommerce.com. Actually, wait, KenB is first name + last initial? No, let me re-examine: KenB@azcommerce.com (Ken Burns) -> First name + Last initial. ShawnN@azcommerce.com (Shawn Neidorf) -> First name + Last initial. KoluW@azcommerce.com (Kolu Wilson) -> First name + Last initial. FernandoG@azcommerce.com (Fernando Garcia) -> First name + Last initial. MelissaL@azcommerce.com (Melissa Lamson) -> First name + Last initial. JenaM@azcommerce.com (Jena Coolidge McGovern) -> First name + Last initial. VicN@azcommerce.com (Vic Narusis) -> First name + Last initial. PatrickP@azcommerce.com (Patrick Ptak) -> First name + Last initial. RyanR@azcommerce.com (Ryan Ruiz) -> First name + Last initial. MarisaW@azcommerce.com (Marisa Walker) -> First name + Last initial. KeithW@azcommerce.com (Keith Watkins) -> First name + Last initial. This is first name + last initial. Wait, the instructions say 'flast' is first initial + last name. Let me check the options again: 'first.last', 'firstlast', 'finitial.last', 'first_last', 'flast', 'last.first', 'firstname'. 'flast' is traditionally first initial + last name. If the pattern is 'First name + Last initial', it's not explicitly in the list. Let me re-read the options. Pattern: first.last / firstlast / finitial.last / first_last / flast / last.first / firstname / NONE_FOUND / CATCH_ALL_UNKNOWN. If it's first name + last initial, and that's not listed, I should check if 'flast' means first initial + last name or if I misread the names. KenB (Ken Burns), ShawnN (Shawn Neidorf). Yes, it's first name + last initial. Since 'first name + last initial' is not an option, I will check if any of the options match better or if I should use 'CATCH_ALL_UNKNOWN' or just describe it in notes. Wait, 'flast' usually means first initial + last name. If the convention is consistently 'Firstname + LastInitial', I should report it as such. However, the available options are limited. Let me look at the emails again. KenB@azcommerce.com. Ken (First) + B (Last Initial). ShawnN@azcommerce.com. Shawn (First) + N (Last Initial). This is very consistent. I'll categorize it as 'CATCH_ALL_UNKNOWN' with a clear note or see if 'flast' was a typo in my head for 'first name last initial'. Actually, the prompt says 'flast' but doesn't define it. Standard industry shorthand 'flast' is first initial last name. If the pattern is FirstnameLastInitial, I'll use 'CATCH_ALL_UNKNOWN' and explain. Wait, let me double check 'firstlast'. No, it's not firstlast. I will use 'CATCH_ALL_UNKNOWN' and describe the pattern 'firstname + last initial'. Wait, is it possible 'flast' is 'firstname + last initial' in this specific task's context? No, usually it's the other way. I will check one more thing. Could it be first name only for some? No, KenB, ShawnN. I'll use 'CATCH_ALL_UNKNOWN' and note the specific pattern. Actually, I'll just pick the closest or use the notes to be precise. Actually, let's look at the list again: 'first.last', 'firstlast', 'finitial.last', 'first_last', 'flast', 'last.first', 'firstname'. None match perfectly. I will use 'CATCH_ALL_UNKNOWN'.

### R05 — Arkansas — The Arkansas Economic Development Commission
- Canonical domain: `arkansasedc.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.arkansasedc.com/leadership
- Sample 1: `coneal@arkansasedc.com` — https://www.arkansasedc.com/employee-detail/clint-o-neal
- Sample 2: `tyler.hale@arkansasedc.com` — https://www.arkansasedc.com/news-events/newsroom
- Pattern: flast | convention_confidence: 40
- Math: Samples found: coneal@arkansasedc.com (Clint O'Neal) and tyler.hale@arkansasedc.com (Tyler Hale). Note that Jennifer Emerson uses JEmerson@ArkansasEDC.com and Jennifer Fowler uses JFowler@ArkansasEDC.com, and Cathy Ma uses CMa@ArkansasEDC.com. The pattern is inconsistent across staff, with some using 'flast' (coneal, jemerson, jfowler, cma) and some using 'first.last' (tyler.hale). However, flast seems more prevalent among leadership and specific divisions. Given the prompt's options, first.last and flast are both present, but flast has more samples (4 vs 1). I will report flast as the primary convention.

### R06 — California — The California Governor's Office of Business and Economic Development
- Canonical domain: `gobiz.ca.gov`
- How confirmed: OFFICIAL_DOC — https://www.linkedin.com/posts/cagobiz_scammers-are-impersonating-the-california-activity-7432929215592718336-R4FC
- Sample 1: `Kaina.Pereira@gobiz.ca.gov` — https://business.ca.gov/wp-content/uploads/2020/04/EDC-COVID-19-Outreach-Webinar-April-2020.pdf
- Sample 2: `Manjeet.McCarthy@gobiz.ca.gov` — https://business.ca.gov/wp-content/uploads/2020/04/EDC-COVID-19-Outreach-Webinar-April-2020.pdf
- Pattern: first.last | convention_confidence: 75
- Math: Found multiple staff email samples using the 'first.last' pattern: Kaina.Pereira@gobiz.ca.gov and Manjeet.McCarthy@gobiz.ca.gov. Another sample Kaitlin.Lewis@business.ca.gov was also found, but official communication explicitly confirms @gobiz.ca.gov is the primary domain for staff. Samples from official PDF and LinkedIn post.

### R07 — Colorado — The Colorado Office of Economic Development and International Trade
- Canonical domain: `state.co.us`
- How confirmed: SITE_PUBLISHED_EMAIL — https://oedit.colorado.gov/emma-acheson
- Sample 1: `emma.acheson@state.co.us` — https://oedit.colorado.gov/emma-acheson
- Sample 2: `samantha.albert@state.co.us` — https://oedit.colorado.gov/samantha-albert
- Pattern: first.last | convention_confidence: 75
- Math: emma.acheson@state.co.us + samantha.albert@state.co.us => first.last. Found 2 samples on official staff bio pages. General inquiry email is oedit.info@state.co.us.

### R08 — Connecticut — The Connecticut Department of Economic and Community Development
- Canonical domain: `ct.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://portal.ct.gov/DECD/Content/About_DECD/Contact
- Sample 1: `Patricia.Paesani@ct.gov` — https://portal.ct.gov/DECD/Content/About_DECD/Contact
- Sample 2: `Sheila.Hummel@ct.gov` — https://portal.ct.gov/DECD/Content/About_DECD/Contact
- Pattern: first.last | convention_confidence: 90
- Math: Patricia.Paesani@ct.gov + Sheila.Hummel@ct.gov => first.last. Found over 10 samples on the contact page following this pattern.

### R09 — Delaware — The Delaware Division of Small Business
- Canonical domain: `delaware.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://business.delaware.gov/contact/
- Sample 1: `Joe.Zilcosky@delaware.gov` — https://business.delaware.gov/team-showcase/joe-zilcosky/
- Sample 2: `Anastasia.Jackson@delaware.gov` — https://business.delaware.gov/team-showcase/anastasia-jackson/
- Pattern: first.last | convention_confidence: 75
- Math: Joe.Zilcosky@delaware.gov + Anastasia.Jackson@delaware.gov => first.last. Found 2 samples on individual staff bio pages. (Gemini.Cornish@delaware.gov also follows this pattern).

### R10 — Florida — FloridaCommerce
- Canonical domain: `commerce.fl.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.floridajobs.org/news-center
- Sample 1: `Heather.Shubirg@Commerce.fl.gov` — https://selectflorida.org/wp-content/uploads/Toolkit-SelectFlorida-Complete.pdf
- Sample 2: `madison.lawson@commerce.fl.gov` — https://globaledge.msu.edu/states/florida/tradecontacts
- Pattern: first.last | convention_confidence: 75
- Math: Found two staff emails: Heather.Shubirg@Commerce.fl.gov and madison.lawson@commerce.fl.gov. Both follow the first.last pattern. The department recently rebranded from DEO (deo.myflorida.com) to FloridaCommerce (commerce.fl.gov), as evidenced by the new official website floridajobs.org prominently displaying the new logo and email addresses.

### R11 — Georgia — The Georgia Department of Economic Development
- Canonical domain: `georgia.org`
- How confirmed: SITE_PUBLISHED_EMAIL — https://georgia.org/about-us/meet-the-department/film-office-contacts
- Sample 1: `jatwell@georgia.org` — https://georgia.org/press-releases/2026/arcelormittal-building-solutions-brings-north-american-hq-macon-bibb
- Sample 2: `lthomas@georgia.org` — https://georgia.org/about-us/meet-the-department/film-office-contacts
- Pattern: finitial.last | convention_confidence: 90
- Math: Multiple samples confirm the pattern. Examples: Jessica Atwell (jatwell@georgia.org) and Lee Thomas (lthomas@georgia.org) both follow the finitial.last pattern.

### R12 — Guam — The Guam Economic Development Authority
- Canonical domain: `investguam.com`
- How confirmed: OFFICIAL_DOC — https://www.investguam.com/wp-content/uploads/2023/STEP/Managing%20Credit%20Options%20for%20Exporters-GEDA%20STEP-May2023.pdf
- Sample 1: `melvin.tabilas@investguam.com` — https://www.investguam.com/wp-content/uploads/2023/STEP/Managing%20Credit%20Options%20for%20Exporters-GEDA%20STEP-May2023.pdf
- Sample 2: `cgarcia@investguam.com` — https://www.investguam.com/wp-content/uploads/2025/Financial%20Reports/CCR%202024_revised%208.22.25.pdf
- Pattern: first.last | convention_confidence: 75
- Math: I found two patterns: 'first.last@investguam.com' (e.g., jay.rojas@investguam.com, melvin.tabilas@investguam.com) and 'finitiallast@investguam.com' (e.g., cgarcia@investguam.com). Given the most recent documents like the 'Managing Credit Options for Exporters' PDF (2023) use 'first.last', and the 'jay.rojas' example also follows this, I have categorized it based on the prominent occurrences. However, 'cgarcia' is a significant counter-example. Based on 'melvin.tabilas@investguam.com' and 'jay.rojas@investguam.com', 'first.last' is a confirmed pattern. 'cgarcia@investguam.com' is also confirmed. I will report 'first.last' as the naming convention.

### R13 — Hawaii — The Hawaii Department of Business, Economic Development & Tourism
- Canonical domain: `hawaii.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://dbedt.hawaii.gov/blog/26-41/
- Sample 1: `lacianne.a.goshi@hawaii.gov` — https://dbedt.hawaii.gov/blog/26-41/
- Sample 2: `lyle.h.fujikawa@hawaii.gov` — https://dbedt.hawaii.gov/blog/26-41/
- Pattern: first.last | convention_confidence: 90
- Math: Found multiple samples: lacianne.a.goshi@hawaii.gov (Laci Goshi), lyle.h.fujikawa@hawaii.gov (Lyle Fujikawa), dennis.t.ling@hawaii.gov (Dennis T. Ling), and jamie.k.lum@hawaii.gov (Jamie K. Lum). These samples show a pattern of first.middleinitial.last@hawaii.gov. However, the standard options provided are limited. Among the choices, the closest matches are 'first.last' or 'finitial.last', but the actual pattern consistently includes the middle initial. Given the choices, 'first.last' is the base structure, but 'finitial.last' is not correct. I will use 'first.last' as the closest naming convention, noting the middle initial inclusion. Wait, looking at the options again: first.last, firstlast, finitial.last, first_last, flast, last.first, firstname. None perfectly match 'first.middleinitial.last'. However, in such cases where a middle initial is present, it's often treated as a variation of 'first.last'. I will select 'first.last' and note the middle initial. Actually, looking at 'lacianne.a.goshi', it is 'first.middle.last'. I will report 'first.last' as the naming convention and explain the middle initial in the notes.

### R14 — Idaho — The Idaho Department of Commerce
- Canonical domain: `commerce.idaho.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://commerce.idaho.gov/contact-us/
- Sample 1: `tom.kealey@commerce.idaho.gov` — https://commerce.idaho.gov/contact-us/
- Sample 2: `jake.reynolds@commerce.idaho.gov` — https://commerce.idaho.gov/contact-us/
- Pattern: first.last | convention_confidence: 75
- Math: Found multiple staff emails on the contact page. Examples: tom.kealey@commerce.idaho.gov and jake.reynolds@commerce.idaho.gov. Both follow the first.last@commerce.idaho.gov pattern.

### R15 — Illinois — The Illinois Department of Commerce and Economic Opportunity
- Canonical domain: `illinois.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://dceo.illinois.gov/oe3/contact-us.html
- Sample 1: `Rebecca.Estrada@Illinois.gov` — https://dceo.illinois.gov/oe3/contact-us.html
- Sample 2: `Diana.Alfaro@illinois.gov` — https://dceo.illinois.gov/oe3/contact-us.html
- Pattern: first.last | convention_confidence: 75
- Math: Found multiple staff emails on the OE3 Team contact page. Samples like Rebecca Estrada (Rebecca.Estrada@Illinois.gov) and Diana Alfaro (Diana.Alfaro@illinois.gov) clearly demonstrate the first.last naming convention. Some emails include a middle initial (e.g., Rebecca.J.Bailey@illinois.gov) for uniqueness, but the standard pattern is first.last.

### R16 — Indiana — The Indiana Economic Development Corporation
- Canonical domain: `iedc.in.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://iedc.in.gov/contact
- Sample 1: `LJagger@iedc.in.gov` — https://iedc.in.gov/contact
- Sample 2: `MSaltanovitz@iedc.in.gov` — https://iedc.in.gov/contact
- Pattern: flast | convention_confidence: 75
- Math: Lindsay Jagger => LJagger@iedc.in.gov; Matt Saltanovitz => MSaltanovitz@iedc.in.gov. Pattern is finitial.last. Note: Roy Martin uses romartin@iedc.in.gov which is a variation (first 2 of first name + last name) but the majority of others follow flast (e.g. LJagger, MSaltanovitz, LWalczak, SSalisbury). However, looking closer: LJagger is Lindsay Jagger, MSaltanovitz is Matt Saltanovitz, LWalczak is Linda Walczak, SSalisbury is Sarah Salisbury. These are all finitial.last. Roy Martin is 'romartin', which is 'ro' (from Roy) + 'martin'. Actually, most others are clearly flast. Wait, let's re-examine: Trevor Lane => TLane, Matthew Menze => MMenze, Shance Sizemore => SSizemore, Stephanie Kabel => SKabel, Andrea Lendy => ALendy. These are all flast. Roy Martin is the outlier. I will stick with flast.

### R17 — Iowa — The Iowa Economic Development Authority
- Canonical domain: `iowaeda.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://directory.iowa.gov/employee/results?LastName=&FirstName=&Title=&PhoneNumber=&Email=&Department=Economic+Development+Authority&Office=&Street=&City=&PostalCode=
- Sample 1: `tammy.agey@iowaeda.com` — https://directory.iowa.gov/employee/results?LastName=&FirstName=&Title=&PhoneNumber=&Email=&Department=Economic+Development+Authority&Office=&Street=&City=&PostalCode=
- Sample 2: `sara.andre@iowaeda.com` — https://directory.iowa.gov/employee/results?LastName=&FirstName=&Title=&PhoneNumber=&Email=&Department=Economic+Development+Authority&Office=&Street=&City=&PostalCode=
- Pattern: first.last | convention_confidence: 75
- Math: tammy.agey@iowaeda.com + sara.andre@iowaeda.com => first.last. Found 102 staff records in the official State of Iowa directory.

### R18 — Kansas — The Kansas Department of Commerce
- Canonical domain: `ks.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.kansascommerce.gov/staff-directory/
- Sample 1: `David.Toland@ks.gov` — https://www.kansascommerce.gov/staff-directory/
- Sample 2: `April.Chiang@ks.gov` — https://www.kansascommerce.gov/staff-directory/
- Pattern: first.last | convention_confidence: 75
- Math: David.Toland@ks.gov (David Toland) and April.Chiang@ks.gov (April Chiang) confirm the first.last pattern. Over 280 staff emails on the directory page follow this convention, with occasional middle initials (e.g., Robert.J.Mclaughlin@ks.gov) or trailing numbers for duplicates (e.g., Jennie.Banta1@ks.gov).

### R19 — Kentucky — The Kentucky Cabinet for Economic Development
- Canonical domain: `ky.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://newkentuckyhome.ky.gov/Home/Staff
- Sample 1: `Jeff.Noel@ky.gov` — https://newkentuckyhome.ky.gov/Home/Staff
- Sample 2: `Kristina.Slattery@ky.gov` — https://newkentuckyhome.ky.gov/Home/Staff
- Pattern: first.last | convention_confidence: 75
- Math: Found over 70 staff email samples on the official staff directory. The dominant pattern is first.last (e.g., Jeff.Noel@ky.gov, Kristina.Slattery@ky.gov). A few older or specific accounts use flast (e.g., dbrock@ky.gov) or include a middle initial (e.g., BradleyL.Popp@ky.gov), but first.last is the clear convention.

### R20 — Louisiana — Louisiana Economic Development
- Canonical domain: `la.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.opportunitylouisiana.gov/about-led/leadership-staff
- Sample 1: `Emma.Wagner@la.gov` — https://www.opportunitylouisiana.gov/public-information/media-inquiries
- Sample 2: `Patrick.Addamus@la.gov` — https://www.opportunitylouisiana.gov/about-led/leadership-staff
- Pattern: first.last | convention_confidence: 75
- Math: Emma.Wagner@la.gov + Patrick.Addamus@la.gov => first.last. The staff directory at https://www.opportunitylouisiana.gov/about-led/leadership-staff shows a consistent first.last pattern across numerous entries (e.g., Michaela.Adegbe@la.gov, Carroll.Akins2@la.gov, rick.allen@la.gov).

### R21 — Maine — The Maine Department of Economic and Community Development
- Canonical domain: `maine.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.maine.gov/decd/business-development/meet-the-team
- Sample 1: `james.nimon@maine.gov` — https://www.maine.gov/decd/business-development/meet-the-team
- Sample 2: `Shae.McGehee@maine.gov` — https://www.maine.gov/decd/business-development/meet-the-team
- Pattern: first.last | convention_confidence: 75
- Math: The staff emails follow a consistent first.last pattern. Examples include james.nimon@maine.gov and Shae.McGehee@maine.gov found on the official staff directory. Other samples like charlotte.mace@maine.gov and deborah.johnson@maine.gov confirm this. Some variations include middle initials (e.g., Eric.P.Weidman@maine.gov) or full legal names (e.g., douglas.ray for Doug Ray).

### R22 — Maryland — The Maryland Department of Commerce
- Canonical domain: `maryland.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://commerce.maryland.gov/commerce/contact-us
- Sample 1: `karen.glennhood@maryland.gov` — https://commerce.maryland.gov/commerce/contact-us
- Sample 2: `ricardo.benn@maryland.gov` — https://msa.maryland.gov/msa/mdmanual/12dbed/html/dbed.html
- Pattern: first.last | convention_confidence: 90
- Math: karen.glennhood@maryland.gov + ricardo.benn@maryland.gov => first.last. Note that mona.miles2@maryland.gov and john.papavasiliou2@maryland.gov also exist, suggesting suffixing for duplicate names, but the base pattern is first.last. Found many samples on the official site and state directory.

### R23 — Massachusetts — The Massachusetts Executive Office of Economic Development
- Canonical domain: `mass.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.mass.gov/orgs/executive-office-of-economic-development
- Sample 1: `Margaret.M.Quackenbush@mass.gov` — https://www.mass.gov/news/healey-driscoll-administration-joins-with-ibm-red-hat-to-launch-ai-accelerator-during-boston-tech-week
- Sample 2: `Robert.McGovern@mass.gov` — https://www.mass.gov/event/notice-of-public-comment-period-for-proposed-new-regulation-2024-04-15t090000-0400-2024-05-06t170000-0400
- Pattern: first.last | convention_confidence: 75
- Math: Margaret.M.Quackenbush@mass.gov (first.m.last) and Robert.McGovern@mass.gov (first.last). Note that Meggie Quackenbush uses Margaret.M.Quackenbush@mass.gov, while Robert McGovern uses Robert.McGovern@mass.gov. The pattern is generally first.last, with some variations for middle initials. Found 2 clear samples on official state pages.

### R24 — Michigan — The Michigan Economic Development Corporation
- Canonical domain: `michigan.org`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.michigan.gov/leo/about/org-structure
- Sample 1: `messerq@michigan.org` — https://www.michigan.gov/leo/about/org-structure
- Sample 2: `schwabv@michigan.org` — https://www.miplace.org/link/7f582f136b4143d7870675d8a0da8ca2.aspx
- Pattern: flast | convention_confidence: 90
- Math: Found multiple samples using the 'lastf' pattern (last name + first initial): messerq@michigan.org (Quentin Messer), huntert1@michigan.org (Tupac A. Hunter), schwabv@michigan.org (Vicki Schwab), holtzp@michigan.org (Paula Holtz). Note: Some entries like 'huntert1' and 'donaldsonc2' include a trailing digit, likely for disambiguation. The domain 'michigan.org' is confirmed as the canonical domain for staff emails for the Michigan Economic Development Corporation (MEDC), despite the primary website being michiganbusiness.org.

### R25 — Minnesota — The Minnesota Department of Employment and Economic Development
- Canonical domain: `state.mn.us`
- How confirmed: SITE_PUBLISHED_EMAIL — https://mn.gov/deed/about/contact-us/headquarters.jsp
- Sample 1: `mary.haugen@state.mn.us` — https://mn.gov/deed/about/contact-us/headquarters.jsp
- Sample 2: `enock.kakuuku@state.mn.us` — https://mn.gov/deed/programs-services/dislocated-worker/scsep/providers/
- Pattern: first.last | convention_confidence: 90
- Math: Mary.Haugen@state.mn.us + Enock.Kakuuku@state.mn.us => first.last. Found multiple samples on official MN DEED contact and provider pages confirming the First.Last pattern at the state.mn.us domain.

### R26 — Mississippi — The Mississippi Development Authority
- Canonical domain: `mississippi.org`
- How confirmed: SITE_PUBLISHED_EMAIL — https://mississippi.org/about/offices/
- Sample 1: `pbesselievre@mississippi.org` — https://mississippi.org/about/offices/
- Sample 2: `shardin@mississippi.org` — https://mississippi.org/wp-content/uploads/2023-CDBG-Implementation-Workshop-Powerpoint.pdf
- Pattern: flast | convention_confidence: 75
- Math: pbesselievre@mississippi.org (Patrick Besselievre) + shardin@mississippi.org (Steve Hardin) => flast. I found over 7 staff emails following this pattern in an official PDF and on the website's office contact page.

### R27 — Missouri — The Missouri Department of Economic Development
- Canonical domain: `ded.mo.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://ded.mo.gov/cdbg/staff-contacts
- Sample 1: `joseph.sanning@ded.mo.gov` — https://ded.mo.gov/cdbg/staff-contacts
- Sample 2: `sara.margan@ded.mo.gov` — https://ded.mo.gov/cdbg/staff-contacts
- Pattern: first.last | convention_confidence: 90
- Math: Found multiple staff emails on the CDBG staff directory page. Samples like joseph.sanning@ded.mo.gov (Joe Sanning) and sara.margan@ded.mo.gov (Sara Margan) prove the first.last naming convention. I observed over 10 samples following this pattern on the same page.

### R28 — Montana — The Montana Department of Commerce
- Canonical domain: `mt.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://commerce.mt.gov/About/Leadership/index
- Sample 1: `marta.bertoglio@mt.gov` — https://commerce.mt.gov/About/Leadership/index
- Sample 2: `mandy.rambo@mt.gov` — https://commerce.mt.gov/About/Leadership/index
- Pattern: first.last | convention_confidence: 75
- Math: Found two staff emails on the leadership page: marta.bertoglio@mt.gov and mandy.rambo@mt.gov. Both follow the first.last@mt.gov pattern.

### R29 — Nebraska — The Nebraska Department of Economic Development
- Canonical domain: `nebraska.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://opportunity.nebraska.gov/contact/
- Sample 1: `maureen.larsen@nebraska.gov` — https://opportunity.nebraska.gov/contact/
- Sample 2: `holly.hartman@nebraska.gov` — https://opportunity.nebraska.gov/contact/
- Pattern: first.last | convention_confidence: 75
- Math: maureen.larsen@nebraska.gov + holly.hartman@nebraska.gov => first.last. Found numerous samples on the official contact page. Note: Some staff use formal names (e.g., richard.dey for Rick Dey) or include middle initials (e.g., lori.a.cole).

### R30 — Nevada — The Nevada Governor's Office of Economic Development
- Canonical domain: `goed.nv.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://goed.nv.gov/goed-team/
- Sample 1: `dstonebarger@goed.nv.gov` — https://goed.nv.gov/goed-team/
- Sample 2: `msheldon@goed.nv.gov` — https://goed.nv.gov/goed-team/
- Pattern: flast | convention_confidence: 75
- Math: Dorian Stonebarger (dstonebarger@goed.nv.gov) and Melanie Sheldon (msheldon@goed.nv.gov) demonstrate the flast (finitial+last) pattern. While some variations like c.smith@goed.nv.gov (finitial.last) and angiem@goed.nv.gov (firstlinitial) were observed, flast is the most common pattern among the staff listed.

### R31 — New Hampshire — The New Hampshire Department of Business and Economic Affairs
- Canonical domain: `livefree.nh.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.nheconomy.com/About-Us/Meet-the-Staff
- Sample 1: `Jeanie.L.Forrester@livefree.nh.gov` — https://www.nheconomy.com/About-Us/Meet-the-Staff
- Sample 2: `hilary.l.ryan@livefree.nh.gov` — https://www.nheconomy.com/About-Us/Meet-the-Staff
- Pattern: first.last | convention_confidence: 75
- Math: Found multiple staff emails on the 'Meet the Staff' page. Most follow the 'first.middleinitial.last@livefree.nh.gov' pattern (e.g., Jeanie.L.Forrester@livefree.nh.gov, hilary.l.ryan@livefree.nh.gov), while some omit the middle initial (e.g., michelle.cruz@livefree.nh.gov). The closest standard naming convention is first.last. Found 40+ samples.

### R32 — New Jersey — The New Jersey Economic Development Authority
- Canonical domain: `njeda.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.njeda.gov/strategic-industry-support/
- Sample 1: `Andrew.Gross@njeda.gov` — https://www.njeda.gov/strategic-industry-support/
- Sample 2: `paul.ceppi@njeda.gov` — https://www.njeda.gov/strategic-industry-support/
- Pattern: first.last | convention_confidence: 75
- Math: Found multiple staff emails: kcoviello@njeda.com (firstinitial.last), paul.ceppi@njeda.gov (first.last), ram.akella@njeda.gov (first.last), jen.becker@njeda.gov (first.last), Andrew.Gross@njeda.gov (first.last). While Kathleen Coviello uses kcoviello@njeda.com, the majority of the current leadership team and other staff listed in the latest press releases and pages use the first.last@njeda.gov format. The older kcoviello@njeda.com may be a legacy address or exception. The confirmed canonical domain is njeda.gov.

### R33 — New Mexico — The New Mexico Economic Development Department
- Canonical domain: `edd.nm.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.edd.newmexico.gov/about-us/directory/
- Sample 1: `Rob.Black@edd.nm.gov` — https://www.edd.newmexico.gov/about-us/directory/
- Sample 2: `Isaac.Romero@edd.nm.gov` — https://www.edd.newmexico.gov/about-us/directory/
- Pattern: first.last | convention_confidence: 75
- Math: rob.black@edd.nm.gov + isaac.romero@edd.nm.gov => first.last. I found more than 20 staff emails in the directory all following the first.last pattern (e.g., Jennifer.Webber, Krystal.Speedy, Tim.Hagaman). Note: Some names use full versions (Elizabeth.Waldrip for Beth Waldrip) and others have numeric suffixes (Lynette.King1) likely for disambiguation, but the primary pattern is first.last.

### R34 — New York — Empire State Development
- Canonical domain: `esd.ny.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://esd.ny.gov/esd-media-center/press-releases/esd-announces-Disney-20th-Century-Studios-the-devil-wears-prada-2-fashion-film-more-than-67-9-million-economic-activity-NY
- Sample 1: `emily.mijatovic@esd.ny.gov` — https://esd.ny.gov/esd-media-center/press-releases/esd-announces-Disney-20th-Century-Studios-the-devil-wears-prada-2-fashion-film-more-than-67-9-million-economic-activity-NY
- Sample 2: `pamm.lent@esd.ny.gov` — https://esd.ny.gov/esd-media-center/press-releases/empire-state-development-rallies-soccer-fans-free-fifa-world-cup
- Pattern: first.last | convention_confidence: 75
- Math: emily.mijatovic@esd.ny.gov + pamm.lent@esd.ny.gov => first.last. Found 4 total staff samples (including Ericka Fang and Laura Magee) all following the first.last pattern.

### R35 — North Carolina — The Economic Development Partnership of North Carolina
- Canonical domain: `edpnc.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://edpnc.com/who-we-are/
- Sample 1: `christopher.chung@edpnc.com` — https://edpnc.com/who-we-are/
- Sample 2: `michael.ebert@edpnc.com` — https://edpnc.com/who-we-are/
- Pattern: first.last | convention_confidence: 90
- Math: Found multiple staff email addresses on the official 'Who We Are' page. christopher.chung@edpnc.com (Christopher Chung) and michael.ebert@edpnc.com (Michael Ebert) demonstrate the first.last pattern. Dozens of other samples on the same page follow this convention. Some department-specific variations exist (e.g., @visitnc.com for tourism), but @edpnc.com is the primary organizational domain.

### R36 — North Dakota — The North Dakota Department of Commerce
- Canonical domain: `nd.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.commerce.nd.gov/contact-us/commerce-team-members/commerce-administrative-team
- Sample 1: `cschilken@nd.gov` — https://www.commerce.nd.gov/contact-us/commerce-team-members/commerce-administrative-team
- Sample 2: `ckemmer@nd.gov` — https://www.commerce.nd.gov/contact-us/commerce-team-members/commerce-administrative-team
- Pattern: flast | convention_confidence: 75
- Math: The primary naming convention is flast (finitiallast). For example, Chris Schilken is cschilken@nd.gov and Corby Kemmer is ckemmer@nd.gov. While the majority of the 15+ staff emails found follow this pattern, some include middle initials (e.g., keralston@nd.gov for Katie Ralston Howe) or use firstlast (e.g., peggyweiss@nd.gov).

### R37 — Northern Mariana Islands — The Department of Commerce for the Commonwealth of the Northern Mariana Islands
- Canonical domain: `commerce.gov.mp`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.commerce.gov.mp/about-us/contact-us
- Sample 1: `jnorita@commerce.gov.mp` — https://content.naic.org/es/node/5576?field_contact_state_department_target_id=1077
- Sample 2: `ttudela@commerce.gov.mp` — https://content.naic.org/es/node/5576?field_contact_state_department_target_id=1077
- Pattern: flast | convention_confidence: 75
- Math: The domain uses a mix of role-based (e.g., secretary.mafnas@commerce.gov.mp, registrar.corp@commerce.gov.mp) and staff-specific emails. Staff emails follow the 'flast' pattern as seen with Jenny C. Norita (jnorita@commerce.gov.mp) and Aristona M. Tudela (ttudela@commerce.gov.mp). I also found marriola@commerce.gov.mp and jfred@commerce.gov.mp which appear to be staff-specific. Found 2 clear individual samples plus several role-based samples.

### R38 — Ohio — The Ohio Department of Development
- Canonical domain: `development.ohio.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://development.ohio.gov/about-us/media-contacts
- Sample 1: `Mason.Waldvogel@development.ohio.gov` — https://development.ohio.gov/about-us/media-contacts
- Sample 2: `Sarah.Wickham@development.ohio.gov` — https://development.ohio.gov/home/news-and-events/all-news/2023-0626-governor-dewine-announces-plans-for-estimated-7-billion-investment-by-amazon-web-services-in-ohio
- Pattern: first.last | convention_confidence: 75
- Math: Found two samples: Mason.Waldvogel@development.ohio.gov and Sarah.Wickham@development.ohio.gov. Both follow the first.last pattern. Naming convention is first.last based on these samples.

### R39 — Oklahoma — The Oklahoma Department of Commerce
- Canonical domain: `okcommerce.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.okcommerce.gov/about-us/press-media-inquires/
- Sample 1: `chase.horn@okcommerce.gov` — https://www.okcommerce.gov/about-us/press-media-inquires/
- Sample 2: `ray.little@okcommerce.gov` — https://oklahoma.gov/business/help/contact.html
- Pattern: first.last | convention_confidence: 75
- Math: chase.horn@okcommerce.gov + ray.little@okcommerce.gov => first.last. Found two samples on official and related state pages.

### R40 — Oregon — Business Oregon
- Canonical domain: `biz.oregon.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.oregon.gov/biz/aboutus/contactus/pages/directory.aspx
- Sample 1: `amber.nabors@biz.oregon.gov` — https://biznews.oregon.gov/acton/rif/14786/s-0990-2606/-/l-0007:5417/l-0007/showPreparedMessage?sid=TV2:1kLrcF7si
- Sample 2: `zak.binshaieg@biz.oregon.gov` — https://www.oregon.gov/biz/aboutus/contactus/pages/directory.aspx
- Pattern: first.last | convention_confidence: 75
- Math: Samples found: amber.nabors@biz.oregon.gov (Amber Nabors) and zak.binshaieg@biz.oregon.gov (Zak Binshaieg). Pattern is first.last. Note that some emails contain middle initials or specific variations (e.g., john.b.hobbs@biz.oregon.gov), but the primary convention is first.last.

### R41 — Pennsylvania — The Pennsylvania Department of Community & Economic Development
- Canonical domain: `pa.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://dced.pa.gov/business-assistance/international/international-contacts-page/
- Sample 1: `dbriel@pa.gov` — https://dced.pa.gov/business-assistance/international/international-contacts-page/
- Sample 2: `jblack@pa.gov` — https://dced.pa.gov/business-assistance/international/international-contacts-page/
- Pattern: flast | convention_confidence: 90
- Math: Staff emails for the PA DCED follow the 'flast' pattern (finitial + lastname @pa.gov). Samples like David Briel (dbriel@pa.gov) and Jennifer Black (jblack@pa.gov) demonstrate this clearly. Other variations such as Aaron Pitts (aarpitts@pa.gov) and Michael O'Rourke (miorourke@pa.gov) appear to use multiple leading letters of the first name, likely for disambiguation within the state-wide @pa.gov domain. Found over 10 samples on official pages.

### R42 — Puerto Rico — The Puerto Rico Department of Economic Development and Commerce
- Canonical domain: `ddec.pr.gov`
- How confirmed: OFFICIAL_DOC — https://docs.pr.gov/files/DDEC/Aviso%20Pu%CC%81blico/RFP%20FINANZAS%20-%20RFP-DDEC-2025-06.pdf
- Sample 1: `naelia.cruz@ddec.pr.gov` — https://docs.pr.gov/files/DDEC/Aviso%20Pu%CC%81blico/RFP%20FINANZAS%20-%20RFP-DDEC-2025-06.pdf
- Sample 2: `soraya.moron@ddec.pr.gov` — https://sidoamerica.org/state/puerto-rico/
- Pattern: first.last | convention_confidence: 75
- Math: Found staff emails naelia.cruz@ddec.pr.gov and soraya.moron@ddec.pr.gov which follow the first.last naming convention. Multiple other examples like luis.mendez@ddec.pr.gov and paola.rosario@ddec.pr.gov were also identified in official documents and search results, confirming the pattern.

### R43 — Rhode Island — Rhode Island Commerce
- Canonical domain: `commerceri.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://commerceri.com/about-us/commerce-staff/
- Sample 1: `daniela.fairchild@commerceri.com` — https://commerceri.com/about-us/commerce-staff/
- Sample 2: `neil.martin@commerceri.com` — https://commerceri.com/about-us/commerce-staff/
- Pattern: first.last | convention_confidence: 90
- Math: daniela.fairchild@commerceri.com + neil.martin@commerceri.com => first.last. The staff directory lists dozens of employees, almost all of whom follow the first.last@commerceri.com pattern.

### R44 — South Carolina — The South Carolina Department of Commerce
- Canonical domain: `sccommerce.com`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.sccommerce.com/contact
- Sample 1: `aclark@sccommerce.com` — https://www.sccommerce.com/contact
- Sample 2: `sdomingues@sccommerce.com` — https://www.sccommerce.com/international/international-business/global-network
- Pattern: flast | convention_confidence: 75
- Math: Found multiple staff emails following the flast pattern: Alex Clark (aclark@sccommerce.com) and Sergio Domingues (sdomingues@sccommerce.com). Other samples include Roxana Gonzalez (rgonzalez@sccommerce.com) and Sam Leng (sleng@sccommerce.com).

### R45 — South Dakota — The South Dakota Governor's Office of Economic Development
- Canonical domain: `sdgoed.com`
- How confirmed: OFFICIAL_DOC — https://boardsandcommissions.sd.gov/bcuploads/REDI%20Board%20Public%20Packet%2008-09-2023.pdf
- Sample 1: `travis.dovre@sdgoed.com` — https://boardsandcommissions.sd.gov/bcuploads/REDI%20Board%20Public%20Packet%2008-09-2023.pdf
- Sample 2: `joe.fiala@sdgoed.com` — https://mylrc.sdlegislature.gov/api/Documents/Attachment/281745.pdf?Year=2025
- Pattern: first.last | convention_confidence: 75
- Math: Found travis.dovre@sdgoed.com and joe.fiala@sdgoed.com which follow the first.last naming convention. Note that some staff also use state.sd.us (e.g., Jennifer.ondell@state.sd.us) which follows the same first.last pattern. The official RFP documents specify @sdgoed.com for inquiries. 2 samples found.

### R46 — Tennessee — The Tennessee Department of Economic and Community Development
- Canonical domain: `tn.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://tnecd.com/meet-the-team/
- Sample 1: `stuart.mcwhorter@tn.gov` — https://tnecd.com/meet-the-team/
- Sample 2: `allen.borden@tn.gov` — https://tnecd.com/meet-the-team/
- Pattern: first.last | convention_confidence: 90
- Math: stuart.mcwhorter@tn.gov + allen.borden@tn.gov => first.last. I found dozens of samples on the department's 'Meet the Team' page, most following the first.last pattern, though some include middle initials when necessary.

### R47 — Texas — The Texas Office of the Governor, Economic Development & Tourism division
- Canonical domain: `gov.texas.gov`
- How confirmed: OFFICIAL_DOC — https://www.nist.gov/document/chips-texas-semiconductor-industry-fact-sheet
- Sample 1: `larry.mcmanus@gov.texas.gov` — https://www.nist.gov/document/chips-texas-semiconductor-industry-fact-sheet
- Sample 2: `shirley.temple@gov.texas.gov` — https://sidoamerica.org/state/texas/
- Pattern: first.last | convention_confidence: 75
- Math: Found two samples: larry.mcmanus@gov.texas.gov and shirley.temple@gov.texas.gov. Both follow the first.last pattern. Naming convention is first.last. Found samples on NIST and SIDO websites which refer to official Texas Economic Development staff.

### R48 — U.S. Virgin Islands — The U.S. Virgin Islands Economic Development Authority
- Canonical domain: `usvieda.org`
- How confirmed: OFFICIAL_DOC — https://usvieda.org/sites/default/files/rfp/Updated_RFP%20-%20Independent%20Compliance%20Officer_01172023_Publication.pdf
- Sample 1: `mabenjamin@usvieda.org` — https://usvieda.org/sites/default/files/rfp/Updated_RFP%20-%20Independent%20Compliance%20Officer_01172023_Publication.pdf
- Sample 2: `kwebbe@usvieda.org` — https://usvieda.org/sites/default/files/rfp/Updated_RFP%20-%20Independent%20Compliance%20Officer_01172023_Publication.pdf
- Pattern: flast | convention_confidence: 75
- Math: I found two clear examples of staff emails: mabenjamin@usvieda.org (Margarita Benjamin) and kwebbe@usvieda.org (Kelly Thompson Webbe). Both follow the 'finitial.last' pattern, though Margarita's includes a middle initial (ma + benjamin). However, another sample 'jforbes@usvieda.org' (Ja’Nelle Forbes) follows the simple 'finitial.last' pattern. Given the variation, 'flast' or 'finitial.last' is the strongest candidate. I will use 'flast' as it covers both single and multiple initials followed by the last name. Actually, 'finitial.last' is the standard way to represent 'first initial(s) + last name' in this context. Wait, the prompt says 'finitial.last' or 'flast'. Let's look at the options: first.last, firstlast, finitial.last, first_last, flast, last.first, firstname. 'flast' usually means first initial + last name. 'finitial.last' usually means first initial . last name. Looking at 'mabenjamin' and 'kwebbe', there is NO dot. So 'firstlast' or 'flast'? 'flast' is the most accurate representation for 'finitial + last name' without a dot. 'mabenjamin' is 'ma' (Margarita A) + 'benjamin'. 'kwebbe' is 'k' (Kelly) + 'webbe'. Both are flast (first initial + last name). Note that Margarita uses two initials.

### R49 — Utah — The Utah Governor's Office of Economic Opportunity
- Canonical domain: `utah.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://business.utah.gov/team/
- Sample 1: `trosander@utah.gov` — https://business.utah.gov/team/
- Sample 2: `aspenorton@utah.gov` — https://business.utah.gov/team/
- Pattern: CATCH_ALL_UNKNOWN | convention_confidence: 25
- Math: The staff directory at business.utah.gov/team/ reveals multiple naming patterns for the utah.gov domain. While flast is common (e.g., trosander@utah.gov for Tara Rosander, nrandall@utah.gov for Natalie Randall), firstlast is also frequently used (e.g., aspenorton@utah.gov for Aspen Orton, aaronprice@utah.gov for Aaron Price). Additionally, some emails include middle initials (e.g., jrmoss@utah.gov for Jefferson Moss). Given this significant variety across the state-wide domain, it is classified as CATCH_ALL_UNKNOWN.

### R50 — Vermont — The Vermont Agency of Commerce and Community Development
- Canonical domain: `vermont.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://accd.vermont.gov/about-us/contact-us
- Sample 1: `lindsay.kurrle@vermont.gov` — https://accd.vermont.gov/about-us/contact-us
- Sample 2: `tayt.brooks@vermont.gov` — https://accd.vermont.gov/about-us/contact-us
- Pattern: first.last | convention_confidence: 90
- Math: The staff directory lists dozens of email addresses. Samples lindsay.kurrle@vermont.gov and tayt.brooks@vermont.gov demonstrate the first.last pattern. While some emails include a middle initial (e.g., kevin.r.lambert@vermont.gov), the predominant convention remains first.last.

### R51 — Virginia — The Virginia Economic Development Partnership
- Canonical domain: `vedp.org`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.vedp.org/staff-directory
- Sample 1: `jelkoubi@vedp.org` — https://www.vedp.org/staff-directory
- Sample 2: `tsniffin@vedp.org` — https://www.vedp.org/staff-directory
- Pattern: flast | convention_confidence: 75
- Math: Jason El Koubi (jelkoubi@vedp.org) and Ted Sniffin (tsniffin@vedp.org) demonstrate the first initial + last name pattern. A total of 4 staff emails were observed on the directory page, all following this convention.

### R52 — Washington — The Washington State Department of Commerce
- Canonical domain: `commerce.wa.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://www.commerce.wa.gov/pwb/about-pwb/
- Sample 1: `Amelia.Lamb@commerce.wa.gov` — https://www.commerce.wa.gov/news/
- Sample 2: `Sheila.Richardson@Commerce.wa.gov` — https://www.commerce.wa.gov/pwb/about-pwb/
- Pattern: first.last | convention_confidence: 75
- Math: Amelia.Lamb@commerce.wa.gov + Sheila.Richardson@commerce.wa.gov => first.last. Numerous staff samples found on the News and Staff information pages confirm this naming convention.

### R53 — West Virginia — The West Virginia Department of Economic Development
- Canonical domain: `wv.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://westvirginia.gov/connect-with-us/meet-the-team/
- Sample 1: `Todd.E.Hooker@wv.gov` — https://westvirginia.gov/connect-with-us/meet-the-team/
- Sample 2: `Angela.Mascia@wv.gov` — https://westvirginia.gov/connect-with-us/meet-the-team/
- Pattern: first.last | convention_confidence: 90
- Math: Found multiple staff emails on the team page. Examples include Todd.E.Hooker@wv.gov and Angela.Mascia@wv.gov. The pattern is first.last, frequently including a middle initial (first.m.last). Both variations use dots as separators. Found over 10 samples on the directory page.

### R54 — Wisconsin — The Wisconsin Economic Development Corporation
- Canonical domain: `wedc.org`
- How confirmed: SITE_PUBLISHED_EMAIL — https://wedc.org/contact-us/staff-directory/
- Sample 1: `david.callender@wedc.org` — https://wedc.org/contact-us/
- Sample 2: `jordan.wohlleber@wedc.org` — https://wedc.org/contact-us/staff-directory/
- Pattern: first.last | convention_confidence: 90
- Math: The pattern is clearly first.last as evidenced by david.callender@wedc.org and jordan.wohlleber@wedc.org. Over 50 samples were found on the staff directory page following this convention, with many using formal first names (e.g., joseph.lawniczak for Joe Lawniczak).

### R55 — Wyoming — The Wyoming Business Council
- Canonical domain: `wyo.gov`
- How confirmed: SITE_PUBLISHED_EMAIL — https://wyomingbusiness.org/about/team/
- Sample 1: `josh.dorrell@wyo.gov` — https://wyomingbusiness.org/about/team/
- Sample 2: `heather.tupper@wyo.gov` — https://wyomingbusiness.org/about/team/
- Pattern: first.last | convention_confidence: 75
- Math: josh.dorrell@wyo.gov + heather.tupper@wyo.gov => first.last. Over 30 staff members listed on the team page follow the first.last pattern, with a few instances of numbers (e.g., emma.gregg1) likely for deduplication.
