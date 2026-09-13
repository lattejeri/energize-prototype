# Energize Industries — Master Website Copy Deck & Content Document

> **Document Type:** Master Website Copy Deck & Content Architecture  
> **Source Baseline:** Prototype v0.3 Schematic Wireframe (`wireframes/prototype_v0.3.html`)  
> **Target Platform:** Custom WordPress Theme / Headless Commercial Web Application  
> **Status:** Approved Baseline Content  
> **Last Updated:** September 2026  
> **Editorial Convention:** Australian English (Sentence Case headings, direct commercial tone, zero filler)

---

## Executive Summary & Content Governance

### 1. Brand Identity & Operating Entity
- **Trading Name:** Energize Industries / Energize
- **Legal Entity:** Energize Electrical Safety Management Pty Ltd
- **ABN:** 39 136 854 754
- **Electrical Contractor Licence:** # 70739 (Queensland Electrical Safety Office)
- **Year Established:** 2003 (20+ Years in Operation)
- **Headquarters:** Unit 2 / 400 Newman Road, Geebung QLD 4034
- **Primary Phone:** (07) 3865 6500
- **Primary Estimating Email:** `estimating@energizeindustries.com`

### 2. Tone of Voice & Messaging Principles
1. **Director-Led Authority:** Dan Monti (Projects) and Jason Edwards (Operations) personally manage commercial contracts and technical delivery on site. Avoid impersonal corporate third-person posturing; highlight working director accessibility and on-site problem solving.
2. **Engineering Rigor:** Every capability statement is substantiated with real Australian Standards (e.g. AS/NZS 3000, AS/NZS 2293, AS ISO 18434-1) and verifiable prequalifications (CM3, Master Electricians, $20M Public Liability).
3. **Head Contractor Alignment:** Messaging specifically addresses the pain points of Head Contractor Estimators, Project Managers, Contract Administrators, and Commercial Facility Managers (e.g. compressed programs, zero unscheduled downtime, latent clash avoidance, defect-free practical completion).
4. **Sentence Case Standard:** All headlines and titles follow clean Australian sentence case (e.g., *“What separates us from the rest?”* instead of *“What Separates Us From The Rest?”*).

---

## Document Navigation (Table of Contents)

1. [Global Components (Header, Nav & Footer)](#global-components)
2. [Template 01: Home (`front-page.php`)](#template-01-home-front-pagephp)
3. [Template 02: Why Energize (`page-why.php`)](#template-02-why-energize-page-whyphp)
4. [Template 03: Services Overview (`page-services.php`)](#template-03-services-overview-page-servicesphp)
5. [Template 04: Service Detail — Infrared Thermal Imaging (`single-service.php`)](#template-04-service-detail--infrared-thermal-imaging-single-servicephp)
6. [Template 05: Work Portfolio (`archive-project.php`)](#template-05-work-portfolio-archive-projectphp)
7. [Template 06: Case Study — Eagle Farm Racecourse (`single-project.php`)](#template-06-case-study--eagle-farm-racecourse-single-projectphp)
8. [Template 07: Contact (`page-contact.php`)](#template-07-contact-page-contactphp)
9. [Template 08: Request a Quote & Tender Submission (`page-quote.php`)](#template-08-request-a-quote--tender-submission-page-quotephp)
10. [Template 09: Download Capability Statement (`page-capability.php`)](#template-09-download-capability-statement-page-capabilityphp)
11. [Cross-Cutting Master Data Banks](#cross-cutting-master-data-banks)
    - [A. Credential & Accreditation Bank](#a-credential--accreditation-bank)
    - [B. Head Contractor & Client Rolodex](#b-head-contractor--client-rolodex)
    - [C. Complete 13-Project Historical Portfolio Master Index](#c-complete-13-project-historical-portfolio-master-index)
    - [D. Australian Standards & Regulatory Framework Index](#d-australian-standards--regulatory-framework-index)
    - [E. Key Personnel & Leadership Directory](#e-key-personnel--leadership-directory)

---

## Global Components

### 1. Global Header & Main Navigation
*Appears across all templates at the top of the viewport.*

| Component / Element | Element Type | Verbatim Copy / Asset Reference | Target / Action | CMS / ACF Field |
| :--- | :--- | :--- | :--- | :--- |
| **Brand Logo** | Vector SVG | Energize Industries Official Brand Vector Logo (Gradient fill) | Link to Home (`/`) | `global_site_logo` |
| **Nav Item 1** | Menu Link | `Home` | Link to `#template-home` | `primary_nav_items[0]` |
| **Nav Item 2** | Menu Link | `Why Energize` | Link to `#template-why` | `primary_nav_items[1]` |
| **Nav Item 3** | Menu Link | `Services` | Link to `#template-services` | `primary_nav_items[2]` |
| **Nav Item 4** | Menu Link | `Work portfolio` | Link to `#template-work` | `primary_nav_items[3]` |
| **Nav Item 5** | Menu Link | `Contact` | Link to `#template-contact` | `primary_nav_items[4]` |
| **Secondary CTA** | Button | `Download capability statement [PDF]` | Link to `#template-capability` | `nav_cta_secondary` |
| **Primary CTA** | Button (High Contrast) | `Request a quote` (with arrow icon `→`) | Link to `#template-quote` | `nav_cta_primary` |

---

### 2. Global Footer
*Appears across all templates at the bottom of the viewport.*

| Section / Column | Element Type | Verbatim Content | CMS / ACF Field |
| :--- | :--- | :--- | :--- |
| **Col 1: Corporate Profile** | Logo Asset | Energize Industries Official Brand Vector Logo | `footer_logo` |
| | Legal Entity Label | `Energize Electrical Safety Management Pty Ltd` | `footer_legal_entity` |
| | Summary Paragraph | `Director-led commercial electrical contracting, in-house design engineering, and statutory safety compliance across Queensland.` | `footer_bio` |
| **Col 2: Capabilities** | Column Heading | `Capabilities` | `footer_menu_title_1` |
| | Nav Link 1 | `Commercial construction` (Links to Services) | `footer_menu_items_1[0]` |
| | Nav Link 2 | `High voltage upgrades` (Links to Services) | `footer_menu_items_1[1]` |
| | Nav Link 3 | `Infrared thermal imaging` (Links to Service Detail) | `footer_menu_items_1[2]` |
| | Nav Link 4 | `Emergency lighting AS 2293` (Links to Services) | `footer_menu_items_1[3]` |
| | Nav Link 5 | `RCD safety switch testing` (Links to Services) | `footer_menu_items_1[4]` |
| **Col 3: Credentials** | Column Heading | `Credentials` | `footer_menu_title_2` |
| | Credential 1 | `Contractor licence # 70739` | `footer_credentials[0]` |
| | Credential 2 | `ABN: 39 136 854 754` | `footer_credentials[1]` |
| | Credential 3 | `Key accreditation e.g. licence or accrediting body` | `footer_credentials[2]` |
| | Credential 4 | `Key accreditation e.g. licence or accrediting body` | `footer_credentials[3]` |
| | Credential 5 | `Key accreditation e.g. licence or accrediting body` | `footer_credentials[4]` |
| **Col 4: Brisbane HQ** | Column Heading | `Brisbane HQ` | `footer_menu_title_3` |
| | Physical Address | `Unit 2 / 400 Newman Road, Geebung QLD 4034` | `footer_address` |
| | Telephone | `Ph: (07) 3865 6500` | `footer_phone` |
| | Estimating Email | `estimating@energizeindustries.com` | `footer_email` |
| | Contextual Link | `Request a commercial quote →` (Links to Quote) | `footer_cta_link` |
| **Bottom Bar** | Copyright Line | `© 2026 Energize Electrical Safety Management Pty Ltd. All rights reserved.` | `footer_copyright` |
| | Baseline Subtext | `Schematic prototype v0.3 • WordPress theme blueprint` | `footer_version` |

---

## Template 01: Home (`front-page.php`)

### Section 1.1: Hero Block & Energize Philosophy Module
*Split 2-column layout: Left column contains high-impact value proposition; Right column features the interactive 3-card Energize Philosophy.*

#### Left Column: Main Value Proposition
- **Pre-Title Eyebrow Tag:** 
- **Main H1 Headline:** `Complete electrical lifecycle delivery`
- **Subheadline / Lead Paragraph:** `In-house engineering, defect-free commercial execution, and accredited safety maintenance. Every project overseen by directors and completed by specialists.`
- **Primary CTA Button:** `Download capability statement [PDF]` → `#template-capability`
- **Secondary CTA Button:** `Request a quote / tender` → `#template-quote`

#### Right Column: The Energize Philosophy Module
- **Module Header Label:** `ENERGIZE PHILOSOPHY`
- **Interactive Microcopy Hint:** `Click/hover to inspect`
- **Card 01:**
  - **Index Number:** `01`
  - **Title (H3):** `Concept`
  - **Description:** `In-house engineering, other things you would like to say about full service`
  - *(Active by default on page load)*
- **Card 02:**
  - **Index Number:** `02`
  - **Title (H3):** `Construction`
  - **Description:** `Full service commercial electrical installation with on-site director oversight.`
- **Card 03:**
  - **Index Number:** `03`
  - **Title (H3):** `Compliance`
  - **Description:** `Anything you want to say here about making compliance easy for your clients`

---

### Section 1.2: Head Contractor Partner Strip
*Trust verification bar showcasing tier-1 commercial builders and clients.*

- **Eyebrow Label:** `Trusted delivery partner to`
- **Partner Badges (6 Items):**
  1. `ADCO`
  2. `Hutchinson Builders`
  3. `Mainbrace`
  4. `Coles Group`
  5. `Woolworths`
  6. `BESIX Watpac`

---

### Section 1.3: Differentiator Grid — "What separates us from the rest?"
*6-card grid detailing Energize’s operational differentiators with custom icons.*

- **Section Headline (H2):** `What separates us from the rest?`

#### Card 1: Director oversight
- **Title (H3):** `Director oversight`
- **Body Copy:** `Founders Dan Monti and Jason Edwards personally manage every commercial contract on site. Engineering decisions without corporate delays.`
- **Visual Asset:** `user-group-simple.svg`

#### Card 2: Zero compromise on safety
- **Title (H3):** `Zero compromise on safety`
- **Body Copy:** `CM3 prequalified, master electricians accredited, and rigorous AS/NZS 4801 compliance frameworks protecting your site records.`
- **Visual Asset:** `shield-check-simple.svg`

#### Card 3: Turnkey certainty
- **Title (H3):** `Turnkey certainty`
- **Body Copy:** `End-to-end delivery from high-voltage substation integration to switchboard fabrication, sub-mains, and final defect-free handover.`
- **Visual Asset:** `bolt-check-simple.svg`

#### Card 4: In-house design
- **Title (H3):** `In-house design`
- **Body Copy:** `Full AutoCAD and Revit drafting, electrical engineering calculations, and value engineering before procurement begins.`
- **Visual Asset:** `compass-drafting-simple.svg`

#### Card 5: Workforce who care
- **Title (H3):** `Workforce who care`
- **Body Copy:** `Directly employed trades, long-term apprentices, and experienced supervisors invested in clean, compliant, quality workmanship.`
- **Visual Asset:** `heart-handshake-simple.svg`

#### Card 6: Rapid quoting
- **Title (H3):** `Rapid quoting`
- **Body Copy:** `Accurate commercial estimates and value-engineered tender alternatives prepared with direct principal contractor rigor.`
- **Visual Asset:** `clock-speed-simple.svg`

---

### Section 1.4: Two Core Capability Arms
*Full-bleed 2-column architectural split dividing commercial construction from compliance maintenance.*

#### Arm 1: Commercial Contracting & Infrastructure
- **Title (H3):** `Commercial contracting & infrastructure`
- **Description:** `Turnkey electrical delivery for major commercial new builds, retail centres, high-voltage changeovers, and fast-track refurbishments.`
- **Deliverables List:**
  - `List of capabilities`
  - `And Deliverables`
  - `Energize provides under this capability arm`
- **Text Link CTA:** `See all of our work →` → `#template-work`
- **Button CTA:** `Submit tender` → `#template-quote`

#### Arm 2: Statutory Safety & Compliance Maintenance
- **Title (H3):** `Statutory safety & compliance maintenance`
- **Description:** `Protect your assets against catastrophic failure and satisfy mandatory underwriter criteria with structured statutory testing regimes.`
- **Deliverables List:**
  - `List of capabilities`
  - `And Deliverables`
  - `Energize provides under this capability arm`
- **Text Link CTA:** `See our full service offering →` → `#template-services`
- **Button CTA:** `Book audit` → `#template-quote`

---

### Section 1.5: Featured Commercial Work
*Marquee case studies establishing track record.*

- **Section Eyebrow:** `Case studies & past performance`
- **Section Headline (H2):** `Featured commercial work`
- **Section Subtext:** `Proven delivery across high-density retail and mission-critical high voltage infrastructure.`
- **Section Action Link:** `Explore all projects →` → `#template-work`

#### Project Card 1: Eagle Farm Racecourse HV upgrade
- **Visual Asset:** `[Large format photo: Eagle Farm Racecourse substation | 800x400]`
- **Sector Tags:** `Venues & stadiums` • `High voltage` • `Nov 2018`
- **Title (H3):** `Eagle Farm Racecourse HV upgrade`
- **Description:** `Description of what Energize did on this job`
- **Action Link:** `Read case study →` → `#template-work-detail`

#### Project Card 2: Coles Pacific Pines fast-track handover
- **Visual Asset:** `[Large format photo: Coles Pacific Pines fitout | 800x400]`
- **Sector Tags:** `Retail & supermarkets` • `Fast-track fitout` • `Nov 2016`
- **Title (H3):** `Coles Pacific Pines fast-track handover`
- **Description:** `Description of what Energize did on this job`
- **Action Link:** `Read case study →` → `#template-work-detail`

---

### Section 1.6: Capability Statement Pre-Footer Block
*2-column callout driving commercial document downloads.*

#### Left Column (Value Overview):
- **Eyebrow Tag:** 
- **Headline (H2):** `Evaluating electrical subcontractors for an upcoming project?`
- **Body Paragraph:** `Download our complete 2026 commercial capability statement containing placeholder information that goes over 2-3 lines.`

#### Right Column (Action Box):
- **Card Title:** `Instant PDF download & tender summary`
- **Card Subtext:** `Directly accessible for head contractor estimators and asset managers.`
- **Button CTA:** `Download capability statement [PDF] →` → `#template-capability`
- **Footnote Accreditations:** `Includes: CM3 Prequalification • Master Electricians Membership • $20M Public Liability`

---

## Template 02: Why Energize (`page-why.php`)

### Section 2.1: Hero Section
- **Eyebrow Tag:** `Why Energize`
- **Main Headline (H1):** `Years in the game. Director led certainty. End-to-end service.`
- **Lead Paragraph:** `Our working director model pairs two decades of hands-on site leadership with full in-house design capabilities and an experienced workforce who take pride in their craft.`

---

### Section 2.2: The 7 Zig-Zag Proof Beats

#### Beat 1: Direct Leadership (Hands-on working director philosophy)
- **Tag:** `01. Direct leadership`
- **Headline (H2):** `Hands-on working director philosophy`
- **Body Copy Paragraph 1:** `Unlike conventional firms where directors remain detached from site operations, co-founders Dan Monti and Jason Edwards personally oversee every project undertaken, regardless of scale.`
- **Body Copy Paragraph 2:** `This gives principal contractors direct access to decision-makers, enables instantaneous on-site problem resolution, and provides foremen with high-level technical backing.`
- **Director Attribution Strip:** `Dan Monti (Projects) • Jason Edwards (Operations)`
- **Visual Asset Placeholder:** `[Large format photo: Working directors Dan Monti & Jason Edwards on commercial site | 800x600]`

#### Beat 2: Design and Construct (In-house design capabilities)
- **Tag:** `02. Design and construct`
- **Headline (H2):** `Full in-house design capabilities`
- **Body Copy Paragraph 1:** `Energize maintains internal drafting and engineering expertise. Through early contractor involvement (ECI), we partner with developers and consulting engineers during schematic phases.`
- **Body Copy Paragraph 2:** `Talk about the competitive advantage that comes from internal design expertise here.`
- **Verification Note:** `Verified in: Customs House 5-Star Green Star office, Coles Silkstone`
- **Visual Asset Placeholder:** `[Technical visual: In-house electrical single line diagram & 3D BIM clash detection | 800x600]`

#### Beat 3: Skilled Workforce (Experienced workforce who care about quality)
- **Tag:** `03. Skilled workforce`
- **Headline (H2):** `An experienced workforce who care about quality`
- **Body Copy Paragraph 1:** `We deploy handpicked, vetted electrical mechanics and technicians who take genuine pride in the quality and safety of their installations.`
- **Body Copy Paragraph 2:** `When site demands change or timelines compress, our teams approach challenges with a proactive, collaborative "we'll get it sorted" delivery attitude that keeps construction programs on schedule.`
- **Embedded Quote Block:**  
  *“Personal note of thanks to you and the boys for the outstanding effort... always most courteous, professional, and cooperative.”*  
  **Attribution:** `— Tom O'Sullivan, Development Manager, Coles Group`
- **Visual Asset Placeholder:** `[Large format photo: Energize licensed electrical trades on commercial installation | 800x600]`

#### Beat 4: Longevity (20+ years in the game across Queensland)
- **Tag:** `04. Longevity`
- **Headline (H2):** `20+ years in the game across Queensland`
- **Body Copy Paragraph 1:** `With over two decades of operation, Energize Industries brings deep familiarity with Queensland network providers (Energex and Ergon Energy), council regulations, and commercial construction environments.`
- **Body Copy Paragraph 2:** `Our proven track record spans metropolitan Brisbane, Gold Coast, Sunshine Coast, Ipswich, Toowoomba, Mackay, Bundaberg, Gladstone, and Moranbah.`
- **Visual Stat Callout Box:**
  - **Large Metric:** `2003`
  - **Label:** `Established in Brisbane`
  - **Subtext:** `Over two decades of commercial contracting across South East Queensland and regional centres.`

#### Beat 5: Safety Governance (Safety as a competitive advantage)
- **Tag:** `05. Safety governance`
- **Headline (H2):** `Safety as a competitive advantage`
- **Body Copy Paragraph:** `At Energize Industries, safety is not a slogan—it is the bedrock of our operating licence. We manage risk proactively so principal contractors and asset managers are fully shielded from liability.`
- **Safety Bullet Points:**
  - `Include relevant safety and compliance`
  - `licence and accreditations`
  - `in this space`
- **Visual Asset Placeholder:** `Any badges or symbols for accreditations e.g. ISO`

#### Beat 6: Accreditations, Licences & Insurances Grid
- **Eyebrow Tag:** `Compliance credentials`
- **Section Headline (H2):** `Licences, accreditations, and insurances`
- **Subtext:** `Full corporate and statutory compliance protecting every project.`
- **6 Compliance Cards:**
  1. **Electrical Licence:** `Contractor lic # 70739` | Authority: `Queensland Electrical Safety Office`
  2. **Industry Association:** `Master Electricians Australia` | Status: `Accredited commercial contracting member`
  3. **Safety Prequalification:** `State safety qualification/s here` | Scope: `Verified WHS risk management systems`
  4. **Public Liability:** `State coverage here` | Underwriting: `State coverage here`
  5. **Workers Compensation:** `WorkCover Queensland` | Status: `Current, verified and fully compliant`
  6. **Corporate Structure:** `ABN: 39 136 854 754` | Entity: `Energize Electrical Safety Management Pty Ltd`

#### Beat 7: Verbatim Head Contractor & Engineer Testimonials
- **Eyebrow Tag:** `Verified commendations`
- **Section Headline (H2):** `What head contractors and engineers say`
- **Testimonial 1:**
  - **Quote:** *“Keith, I felt confident having you coordinate the major shutdowns... It was a difficult project with potential to shut down the inner-city network with substantial financial consequence to Energex. We completed the project on budget with no major incident or injury.”*
  - **Name:** `Carlo Martelli`
  - **Title/Company:** `General Manager, Ranbury (Victoria Park Infrastructure)`
- **Testimonial 2:**
  - **Quote:** *“I know the changes were coming thick and fast towards the end and it was due to your ‘we’ll get it sorted’ attitude that got us across the line on time. A truly great team. Look forward to seeing you on the next Coles property project.”*
  - **Name:** `Tom O'Sullivan`
  - **Title/Company:** `Development Manager, Coles Group (Coles Pacific Pines)`
- **Testimonial 3:**
  - **Quote:** *“We would like to express our appreciation to Energize for their performance on the Eagle Farm Racecourse Electrical Upgrade Project.”*
  - **Name:** `Michael Bourke`
  - **Title/Company:** `Wood & Grieve Engineers (Eagle Farm Racecourse)`

---

### Section 2.3: Contextual Action Callout
- **Headline (H3):** `Partner with a contractor that protects your program and safety`
- **Subtext:** `Download our complete 12-page commercial capability statement.`
- **Button CTA:** `Download capability statement [PDF]` → `#template-capability`

---

## Template 03: Services Overview (`page-services.php`)

### Section 3.1: Hero Section
- **Eyebrow Tag:** `Commercial capabilities`
- **Main Headline (H1):** `Complete turnkey electrical contracting and compliance`
- **Lead Paragraph:** `Energize combines full in-house design capabilities (ECI & D&C) with an experienced workforce who care about the quality of their work. Every commercial package is personally overseen by founding directors Dan Monti and Jason Edwards.`
- **Primary CTA:** `Request a quote / submit tender` → `#template-quote`
- **Secondary CTA:** `Download capability statement [PDF]` → `#template-capability`

---

### Section 3.2: Category 01 — Statutory Compliance & Asset Risk Maintenance
- **Category Badge:** `Category 01`
- **Category Title (H2):** `Fulfill conformance and statutory requirements`
- **Category Subhead:** `Scheduled testing, auditing, and certification ensuring full compliance with Australian Standards and underwriter criteria.`

#### Service 01: Infrared thermal imaging
- **Title (H3):** `Infrared thermal imaging`
- **Description:** `Live switchboard radiometric scanning detecting hot spots and overloaded phases before catastrophic fire. Fulfills mandatory insurer underwriting criteria without operational shutdown.`
- **Standard Tag:** `AS ISO 18434-1`
- **Link CTA:** `View service →` → `#template-service-detail`

#### Service 02: Emergency & exit lighting testing
- **Title (H3):** `Emergency & exit lighting testing`
- **Description:** `Mandatory 6-monthly 90-minute battery discharge tests, luminaire replacement, and automated compliance logbooks ready for council and fire brigade audits.`
- **Standard Tag:** `AS/NZS 2293`
- **Link CTA:** `View service →` → `#template-service-detail`

#### Service 03: RCD safety switch testing
- **Title (H3):** `RCD safety switch testing`
- **Description:** `Precision millisecond trip-time testing verifying disconnection thresholds to protect personnel from lethal electrocution and satisfy WorkSafe obligations.`
- **Standard Tag:** `AS/NZS 3760`
- **Link CTA:** `View service →` → `#template-service-detail`

#### Service 04: Electrical safety audits & RCBO upgrades
- **Title (H3):** `Electrical safety audits & RCBO upgrades`
- **Description:** `Comprehensive hazard evaluation replacing obsolete switchboards and dangerous ceramic rewireable fuses with modern modular RCBO protection.`
- **Standard Tag:** `AS/NZS 3000`
- **Link CTA:** `View service →` → `#template-service-detail`

#### Service 05: Portable appliance test and tag
- **Title (H3):** `Portable appliance test and tag`
- **Description:** `Itemized inspection and electrical parameter testing of single and polyphase portable equipment with non-reusable compliance tags and electronic logbooks.`
- **Standard Tag:** `AS/NZS 3760 & 3012`
- **Link CTA:** `View service →` → `#template-service-detail`

---

### Section 3.3: Category 02 — Design & Construct (ECI & Value Engineering)
- **Category Badge:** `Category 02`
- **Category Title (H2):** `Eliminate engineering clashes and reduce project CAPEX`
- **Category Subhead:** `Upfront engineering involvement and turnkey design resolving problems before they reach the job site.`

#### Service 06: Early contractor involvement (ECI) & design and construct (D&C)
- **Title (H3):** `Early contractor involvement (ECI) & design and construct (D&C)`
- **Description:** `Partnering with developers and head contractors at initial planning stages to audit designs, evaluate constructability, resolve clashes, and identify substantial cost-saving engineering alternatives.`
- **Project Proof Tag:** `Verified in: Customs House Green Star Office, Coles Silkstone`
- **Link CTA:** `Explore D&C capabilities →` → `#template-service-detail`

#### Service 07: Energy-efficient lighting auditing & LED upgrades
- **Title (H3):** `Energy-efficient lighting auditing & LED upgrades`
- **Description:** `Detailed photometric evaluations replacing legacy high-consumption luminaires with commercial solid-state LED systems—cutting lighting energy by up to 70–88% and eliminating ongoing relamping costs.`
- **Longevity Tag:** `Longevity: Commercial LEDs rated up to 50,000 continuous hours`
- **Link CTA:** `Explore lighting upgrades →` → `#template-service-detail`

---

### Section 3.4: Category 03 — Operational Continuity & High-Voltage Infrastructure
- **Category Badge:** `Category 03`
- **Category Title (H2):** `Minimize operational downtime and manage live risk`
- **Category Subhead:** `Executing complex shutdowns, main switchboard replacements, and live changeovers with zero unscheduled outage.`

#### Service 08: High voltage (HV) & substation integration
- **Title (H3):** `High voltage (HV) & substation integration`
- **Description:** `Complex network shutdowns, Energex liaison, transformer augmentation, and high-voltage conduit reticulation managed with zero incident.`
- **Link CTA:** `View HV capabilities →` → `#template-service-detail`

#### Service 09: Main switchboard (MSB) changeovers
- **Title (H3):** `Main switchboard (MSB) changeovers`
- **Description:** `Live-environment switchboard replacements staged out-of-hours to ensure complete continuity of tenant operations.`
- **Link CTA:** `View MSB services →` → `#template-service-detail`

#### Service 10: Commercial construction & fitouts
- **Title (H3):** `Commercial construction & fitouts`
- **Description:** `Supermarket packages, retail tenancies, warehouse distribution centres, and institutional builds delivered on compressed programs.`
- **Link CTA:** `View construction →` → `#template-service-detail`

---

### Section 3.5: Capability Statement Pre-Footer Block
*2-column callout driving commercial document downloads.*

#### Left Column (Value Overview):
- **Eyebrow Tag:** 
- **Headline (H2):** `Evaluating electrical subcontractors for an upcoming project?`
- **Body Paragraph:** `Download our complete 2026 commercial capability statement containing placeholder information that goes over 2-3 lines.`

#### Right Column (Action Box):
- **Card Title:** `Instant PDF download & tender summary`
- **Button CTA:** `Download capability statement [PDF] →` → `#template-capability`

---

## Template 04: Service Detail — Infrared Thermal Imaging (`single-service.php`)

### Section 4.1: Hero Section
- **Breadcrumb Trail:** `Services > Statutory safety & compliance > Infrared thermal imaging`
- **Category Badge:** `Statutory compliance & fire prevention`
- **Main Headline (H1):** `Infrared thermal switchboard imaging and predictive fault prevention`
- **Lead Paragraph:** `Fulfill mandatory commercial property insurance underwriting requirements and protect your facility against catastrophic electrical switchboard fires. Live radiometric scanning with zero operational downtime.`
- **Primary CTA:** `Request a quote for this service` → `#template-quote`
- **Secondary CTA:** `Download sample thermal report layout [PDF]`

---

### Section 4.2: Block 1 — Business Impact & Executive Summary
- **Eyebrow Tag:** `Business impact`
- **Headline (H2):** `Measurable commercial outcomes for facility and asset managers`

#### 4 Measurable Outcome Cards:
1. **01. Underwriter compliance**
   - **Benefit Title:** `Insurance validity`
   - **Description:** `Satisfies mandatory property underwriter criteria required for business interruption coverage.`
2. **02. Zero business disruption**
   - **Benefit Title:** `100% live scanning`
   - **Description:** `Executed during peak operating hours under normal load without plant or tenant power shutdowns.`
3. **03. Fire prevention**
   - **Benefit Title:** `Early fault detection`
   - **Description:** `Detects high-resistance joints and overloaded busbars prior to catastrophic component failure.`
4. **04. Cost reduction**
   - **Benefit Title:** `Planned maintenance`
   - **Description:** `Prioritizes rectifications so repairs are scheduled proactively rather than under emergency callout rates.`

---

### Section 4.3: Block 2 — Persona Mapping
- **Eyebrow Tag:** `Stakeholder alignment`
- **Headline (H2):** `Why infrared scanning is critical for your role`

#### Column 1: For Commercial Facility & Property Managers
- **Audience Label:** `For commercial facility & property managers`
- **Title (H3):** `Eliminate liability and preserve asset continuity`
- **Description:** `A switchboard failure stops operations and exposes asset owners to severe tenant compensation claims. Periodic thermal audits provide verifiable audit trails that prove due diligence to executive boards and insurers.`
- **Key Deliverable Bullet:** `• Complete itemized asset registers provided after every inspection`

#### Column 2: For Head Contractors & Project Engineers
- **Audience Label:** `For head contractors & project engineers`
- **Title (H3):** `Defect-free baseline commissioning`
- **Description:** `Conducting thermal scans during practical completion verifies that newly installed main switchboards, sub-mains, and breaker terminations operate under balanced phase load with zero latent manufacturing defects.`
- **Key Deliverable Bullet:** `• Baseline temperature records embedded into handover documentation`

---

### Section 4.4: Block 3 — Technical Process Steps
- **Eyebrow Tag:** `Inspection protocol`
- **Headline (H2):** `Our three-stage thermographic process`

#### Step 01: Live radiometric scan [PLEASE CHECK]
- **Index:** `01`
- **Title (H3):** `Live radiometric scan`
- **Description:** `High-resolution radiometric infrared cameras paired with calibrated optical reference photos scan all switchboards, busbars, and contactors under normal operational load.`

#### Step 02: Delta-T anomaly evaluation [PLEASE CHECK]
- **Index:** `02`
- **Title (H3):** `Delta-T anomaly evaluation`
- **Description:** `Measuring heat rise (ΔT) above ambient and phase baseline to isolate loose terminations, internal component fatigue, or unbalanced electrical phases.`

#### Step 03: Prioritized remedial dossier [PLEASE CHECK]
- **Index:** `03`
- **Title (H3):** `Prioritized remedial dossier`
- **Description:** `Provision of a searchable digital report with side-by-side thermal/optical photos, exact temperature metrics, and categorized rectifications (Immediate, Urgent, Monitor).`

---

### Section 4.5: Block 4 — Advantage Taxonomy Grid
- **Eyebrow Tag:** `Service advantages`
- **Headline (H2):** `Key advantages of Energize thermography [PLEASE CHECK]`

#### 6 Advantage Cards:
1. **Non-destructive & non-invasive:** `Completed entirely without dismantling switchboard internals or disrupting live commercial operations.`
2. **Underwriter-ready reporting:** `Formatted specifically to satisfy property insurer compliance guidelines and annual renewal checklists.`
3. **Eliminates fire hazards:** `Identifies high-resistance hot spots that are the primary root cause of commercial switchboard fires.`
4. **Quantified Delta-T analysis:** `Precise temperature delta benchmarking ensuring only genuine faults are recommended for replacement.`
5. **Licensed electrical trades:** `All thermography conducted exclusively by qualified electricians who understand switchboard anatomy.`
6. **Direct remedial rectifications:** `Ability to immediately quote, schedule, and safely execute any required breaker replacements or retorquing.`

---

### Section 4.6: Block 5 — Regulatory Framework & Standards
- **Eyebrow Tag:** `Regulatory framework`
- **Headline (H2):** `Applicable standards and governance [PLEASE CHECK]`

#### Standards Cards (3 Items):
1. **Standard:** `AS ISO 18434-1`  
   *Title:* `Condition monitoring and diagnostics of machine systems — Thermography`
2. **Standard:** `AS/NZS 3000:2018`  
   *Title:* `Electrical installations (known as the Australian/New Zealand Wiring Rules)`
3. **Legislation:** `Electrical Safety Act 2002`  
   *Title:* `Queensland Electrical Safety Regulation & WHS Act compliance`

---

### Section 4.7: Block 6 — Verified Projects Track Record
- **Eyebrow Tag:** `Track record`
- **Headline (H2):** `Verified projects utilizing this capability [we will need to map which services we used for each project to achieve this]`
- **Portfolio Link:** `Explore portfolio →` → `#template-work`

#### Project Cards:
1. **Eagle Farm Racecourse** (Client: Brisbane Racing Club)  
   *Scope:* `Main switchboard baseline thermography following HV upgrade.`
2. **Lindsay Transport DC, Acacia Ridge** (Client: Rohrig)  
   *Scope:* `Cold logistics distribution boards and sub-mains thermal testing.`
3. **Suncorp Stadium** (Client: Watpac)  
   *Scope:* `Flood recovery remediation and switchgear safety scans.`

---

### Section 4.8: Block 7 — Contextual Quote Callout
- **Headline (H3):** `Ready to schedule your facility thermal imaging inspection?`
- **Subtext:** `Direct quote provided within 4 hours by Director Dan Monti.`
- **Button CTA:** `Request a thermal audit quote` → `#template-quote`

---

## Template 05: Work Portfolio (`archive-project.php`)

### Section 5.1: Hero Section
- **Eyebrow Tag:** `Past performance`
- **Main Headline (H1):** `Proven track record across Queensland's commercial landscape`
- **Lead Paragraph:** `Over 50 major commercial packages delivered across retail, logistics, education, hospitality, and institutional infrastructure with zero safety compromise.`

---

### Section 5.2: Client Logo Strip
- **Eyebrow Subtext:** `Commercial head contractors & clients`
- **Builder Placeholders (8 Items):** `ADCO`, `Hutchinson`, `Mainbrace`, `Coles`, `Woolworths`, `BESIX Watpac`, `Rohrig`, `FKG Group`

---

### Section 5.3: Marquee Featured Case Studies (Tier 1)
- **Eyebrow Tag:** `Featured delivery`
- **Section Headline (H2):** `Marquee case studies – we'll need to develop some content for these based on what work was done`
- **Subhead:** `Detailed past performance backed by signed head contractor commendations.`

#### Case Study 1: Eagle Farm Racecourse – High voltage & site MSB upgrade [DUMMY CONTENT]
- **Visual Asset Placeholder:** `[Large format photo: Eagle Farm Racecourse substation installation | 800x400]`
- **Sector Badges:** `Stadiums & venues` • `High voltage` • `Ascot • Nov 2018`
- **Headline (H3):** `Eagle Farm Racecourse – High voltage & site MSB upgrade`
- **Description:** `Major high voltage network upgrade, main switchboard installation, and sub-mains reticulation. Commended by Wood & Grieve Engineers.`
- **Action Link:** `Read case study →` → `#template-work-detail`

#### Case Study 2: Coles Pacific Pines – Fast-track supermarket fitout [DUMMY CONTENT]
- **Visual Asset Placeholder:** `[Large format photo: Coles Pacific Pines retail store | 800x400]`
- **Sector Badges:** `Retail & supermarkets` • `Fast-track handover` • `Gold Coast • Nov 2016`
- **Headline (H3):** `Coles Pacific Pines – Fast-track supermarket fitout`
- **Description:** `Full supermarket electrical package delivered defect-free under compressed timelines for ADCO Constructions and Coles Group.`
- **Action Link:** `Read case study →` → `#template-work-detail`

#### Case Study 3: Victoria Park – High-risk network shutdown coordination [DUMMY CONTENT]
- **Visual Asset Placeholder:** `[Large format photo: Victoria Park infrastructure works | 800x400]`
- **Sector Badges:** `Major infrastructure` • `Energex shutdown` • `Brisbane • Jan 2016`
- **Headline (H3):** `Victoria Park – High-risk network shutdown coordination`
- **Description:** `Governing electrical/comms shutdown with zero incident or injury, avoiding inner-city network disruptions. Commended by Ranbury.`
- **Action Link:** `Read case study →` → `#template-work-detail`

#### Case Study 4: Bond University – Business and law faculty buildings
- **Visual Asset Placeholder:** `[Large format photo: Bond University Faculty buildings | 800x400]`
- **Sector Badges:** `Tertiary education` • `ADCO Constructions` • `Gold Coast • 2017`
- **Headline (H3):** `Bond University – Business and law faculty buildings`
- **Description:** `Advanced learning hub and faculty lecture theatre electrical installations delivered across two staged commercial packages.`
- **Action Link:** `Read case study →` → `#template-work-detail`

---

### Section 5.4: Extended Commercial Delivery Portfolio (Tier 2)
- **Eyebrow Tag:** `Completed contracts`
- **Section Headline (H2):** `Additional completed commercial works - we will need to develop a small project description for each of these`
- **Subhead:** `A cross-section of delivered contracts across Queensland.`

#### 9 Commercial Delivery Cards:
1. **Marsden Park Shopping Centre**
   - Head Contractor / Year: `Mainbrace Constructions • 2018`
   - Description: `Commercial shopping centre retail refurbishment.`
   - Tag: `Retail refurbishment`
2. **Albany Creek Shopping Centre**
   - Head Contractor / Year: `Mainbrace Constructions • 2018`
   - Description: `Commercial retail refurbishment and tenancy fitouts.`
   - Tag: `Retail fitout`
3. **QPS Tactical Response Unit**
   - Head Contractor / Year: `ADCO Constructions • 2018`
   - Description: `Queensland Police Service high-security specialized facility.`
   - Tag: `Government & security`
4. **Belmont Shooting Complex**
   - Head Contractor / Year: `Broad Constructions • 2017`
   - Description: `Major sporting infrastructure and shooting range complex.`
   - Tag: `Sports infrastructure`
5. **Lindsay Transport DC, Acacia Ridge**
   - Head Contractor / Year: `Rohrig • 2016`
   - Description: `Major cold storage and heavy transport logistics facility.`
   - Tag: `Logistics & cold storage`
6. **Spectrum Apartments, Lutwyche**
   - Head Contractor / Year: `Badge Constructions • 2016`
   - Description: `Multi-residential medium-density apartment complex.`
   - Tag: `Multi-residential`
7. **Woolworths Banyo**
   - Head Contractor / Year: `ADCO Constructions • 2016`
   - Description: `Supermarket construction and energy-efficient lighting.`
   - Tag: `Supermarket new build`
8. **Dan Murphy's Oxley**
   - Head Contractor / Year: `Stokes Wheeler • 2015`
   - Description: `Large-format liquor retail fitout and refrigeration power.`
   - Tag: `Commercial retail`
9. **Suncorp Stadium flood refurbishment**
   - Head Contractor / Year: `Watpac • 2011`
   - Description: `Ground-level electrical remediation and switchgear restoration.`
   - Tag: `Disaster remediation`

---

### Section 5.5: Contextual Action Callout
- **Headline (H3):** `Require specific project datasheets, subcontractor insurances, or referee contacts?`
- **Subhead:** `Our complete capability statement includes full historical project sheets.`
- **Button CTA:** `Download 2026 capability statement [PDF]` → `#template-capability`

---

## Template 06: Case Study — Eagle Farm Racecourse (`single-project.php`)

### Section 6.1: Project Factsheet Hero
- **Breadcrumb Trail:** `Work portfolio > Stadiums & venues > Eagle Farm Racecourse`
- **Category Badge:** `Commercial infrastructure package`
- **Main Headline (H1):** `Eagle Farm Racecourse – High voltage & site MSB upgrade`
- **Key Project Parameters:**
  - **Client:** `Brisbane Racing Club`
  - **Consulting Engineer:** `Wood & Grieve Engineers`
  - **Location:** `Ascot, Queensland`
  - **Completed:** `November 2018`
- **Photography Placeholder:** `[High-resolution photography: Eagle Farm switchroom & high voltage substation installation | 1440x600]`

---

### Section 6.2: Operational Narrative

#### Section 1: The Challenge
- **Tag:** `Operational context`
- **Headline (H2):** `The challenge - dummy content`
- **Narrative:** `Upgrading legacy electrical infrastructure across a premier racing and entertainment venue while keeping facilities fully operational. There was zero tolerance for unplanned power outages that could disrupt horse training schedules, hospitality venues, or live racing broadcasts.`

#### Section 2: The Energize Turnkey Solution
- **Tag:** `Turnkey delivery`
- **Headline (H2):** `The Energize turnkey solution - dummy content`
- **Narrative Paragraph 1:** `Managing Director Dan Monti personally coordinated the staged live-environment changeovers out-of-hours in direct collaboration with local network authority Energex and consulting engineers Wood & Grieve.`
- **Narrative Paragraph 2:** `Our team engineered temporary power bypasses, pulled heavy sub-main cabling, installed the new site main switchboard (MSB), and verified all protection settings prior to full system cutover.`

#### Section 3: Energize Services Delivered on this Contract
- **Headline (H3):** `Energize services delivered on this contract [PLEASE CHECK]`
- **Deliverables List:**
  - `High voltage (HV) upgrade & substation integration`
  - `Main switchboard (MSB) fabrication & live changeover`
  - `Site-wide sub-mains conduit reticulation`
  - `Energex network authority liaison & outage management`
  - `Infrared thermal imaging baseline commissioning`
  - `As-built electrical drafting & statutory certification`

#### Section 4: Verbatim Engineer Commendation
- **Eyebrow Tag:** `Letter of appreciation`
- **Quote Block:** *“We would like to express our appreciation to Energize for their performance on the Eagle Farm Racecourse Electrical Upgrade Project.”*
- **Signatory Attribution:** `Michael Bourke — Wood & Grieve Engineers`

---

### Section 6.3: Contextual Action Callout
- **Headline (H3):** `Planning a similar commercial infrastructure or switchboard upgrade?`
- **Subtext:** `Discuss constructability and staging with our directors.`
- **Button CTA:** `Request a quote for similar works` → `#template-quote`

---

## Template 07: Contact (`page-contact.php`)

### Section 7.1: Hero Section
- **Eyebrow Tag:** `Direct channels`
- **Main Headline (H1):** `Direct leadership contact across Queensland`
- **Lead Paragraph:** `No gatekeepers or automated phone loops. Direct access to our directors and estimating department.`

---

### Section 7.2: Leadership Directory & Key Contacts Roster
- **Eyebrow Tag:** `Leadership directory`
- **Section Headline (H2):** `Key contacts and departments`

#### Contact Card 1: Dan Monti
- **Visual Placeholder:** `[PHOTO: Dan Monti]`
- **Name (H3):** `Dan Monti`
- **Role Title:** `Managing Director / Projects`
- **Direct Mobile:** `0413 807 060`
- **Direct Email:** `dan@energizeindustries.com`
- **Operational Focus:** `Site governance, technical delivery, major contracts`

#### Contact Card 2: Jason Edwards
- **Visual Placeholder:** `[PHOTO: Jason Edwards]`
- **Name (H3):** `Jason Edwards`
- **Role Title:** `Managing Director / Operations`
- **Direct Office Phone:** `(07) 3865 6500`
- **Direct Email:** `jason@energizeindustries.com`
- **Operational Focus:** `Corporate compliance, safety systems, contracts`

#### Contact Card 3: John Byatt
- **Visual Placeholder:** `[PHOTO: John Byatt]`
- **Name (H3):** `John Byatt`
- **Role Title:** `Sales & Commercial BDM`
- **Direct Mobile:** `0460 024 138`
- **Direct Email:** `john@energizeindustries.com`
- **Operational Focus:** `New business proposals, contractor onboarding`

#### Contact Card 4: Estimating Department
- **Visual Placeholder:** `[DESK: Estimating Team]`
- **Department Name (H3):** `Estimating Department`
- **Role Title:** `Commercial Tenders`
- **Direct Office Phone:** `(07) 3865 6500`
- **Direct Email:** `estimating@energizeindustries.com`
- **SLA Commitment:** `SLA: 4-hour formal tender acknowledgement`

---

### Section 7.3: Direct Inquiry Form & Corporate Headquarters

#### Column 1: Send an Online Inquiry (Form)
- **Form Heading (H3):** `Send an online inquiry`
- **Field 1 (Text):**
  - **Label:** `Full name *`
  - **Placeholder:** `Your name`
  - **Validation:** Required
- **Field 2 (Text):**
  - **Label:** `Company / organization *`
  - **Placeholder:** `Head contractor / facility`
  - **Validation:** Required
- **Field 3 (Email):**
  - **Label:** `Work email *`
  - **Placeholder:** `name@company.com`
  - **Validation:** Required
- **Field 4 (Telephone):**
  - **Label:** `Phone number *`
  - **Placeholder:** `0400 000 000`
  - **Validation:** Required
- **Field 5 (Dropdown Select):**
  - **Label:** `Nature of enquiry`
  - **Options:**
    1. `Commercial tender / project pricing`
    2. `Statutory compliance testing (Thermal, RCD, Lighting)`
    3. `Capability statement request`
    4. `General inquiry`
- **Field 6 (Textarea):**
  - **Label:** `Message`
  - **Placeholder:** `Outline your project scope or maintenance requirements...`
- **Submit Button:** `Send message`

#### Column 2: Corporate Headquarters & Operational Reach
- **Card 1: Corporate Headquarters**
  - **Heading (H3):** `Corporate headquarters`
  - **Physical Address:** `Unit 2 / 400 Newman Road, Geebung QLD 4034`
  - **Postal Address:** `PO Box 179, Geebung QLD 4034`
  - **ABN:** `39 136 854 754`
  - **Electrical Licence:** `70739 (Queensland)`
  - **Switchboard:** `(07) 3865 6500`
  - **Map Visual Placeholder:** `[Interactive map: Geebung Brisbane headquarters | 600x300]`
- **Card 2: Statewide Operational Reach**
  - **Card Heading:** `Statewide operational reach`
  - **Description:** `Headquartered in Brisbane, our service footprint covers Greater Brisbane, Gold Coast, Sunshine Coast, Ipswich, Toowoomba, Mackay, Bundaberg, Gladstone, Moranbah, and regional Queensland.`

---

## Template 08: Request a Quote & Tender Submission (`page-quote.php`)

### Section 8.1: Hero Section
- **Eyebrow Tag:** `Dedicated intake page`
- **Main Headline (H1):** `Request a commercial project quote or submit tender`
- **Lead Paragraph:** `Reviewed directly by Managing Directors Dan Monti and Jason Edwards with a guaranteed 4-hour business acknowledgement SLA.`

---

### Section 8.2: Quote Intake Form & Tender Uploader

#### Dual Track Switcher Toggle
- **Track 1 Button (Active by default):** `Commercial construction / tender`
- **Track 2 Button:** `Statutory safety & compliance`

#### General Estimating Contact Fields
- **Field 1 (Text):**
  - **Label:** `Your name *`
  - **Placeholder:** `Estimator / Project manager`
  - **Validation:** Required
- **Field 2 (Text):**
  - **Label:** `Company / builder name *`
  - **Placeholder:** `Principal contractor / developer`
  - **Validation:** Required
- **Field 3 (Email):**
  - **Label:** `Work email address *`
  - **Placeholder:** `name@builder.com`
  - **Validation:** Required
- **Field 4 (Telephone):**
  - **Label:** `Direct phone number *`
  - **Placeholder:** `0400 000 000`
  - **Validation:** Required

#### Tender-Specific Fields (`#page-tender-fields`)
- **Field 5 (Text):**
  - **Label:** `Project name & site address`
  - **Placeholder:** `e.g. Commercial Hub, Geebung`
- **Field 6 (Date):**
  - **Label:** `Tender submission deadline`
- **Field 7 (File Upload Dropzone):**
  - **Label:** `Upload electrical drawings, specifications or BOQ (PDF, DWG, ZIP up to 50MB)`
  - **Dropzone Prompt:** `Drag and drop tender files here or click to browse`

#### Form Footer & Submission
- **Accreditation Trust Tag:** `Licence: #70739 • Master Electricians • $20M PL`
- **Submit Button:** `Submit tender package`

---

## Template 09: Download Capability Statement (`page-capability.php`)

### Section 9.1: Hero Section
- **Eyebrow Tag:** `2026 Commercial dossier`
- **Main Headline (H1):** `Download the Energize Industries capability statement`
- **Lead Paragraph:** `Complete commercial contracting overview, past project performance sheets, insurance certificates, and WHS management systems.`

---

### Section 9.2: Download Gate Form & Value Highlights

#### Value Matrix Highlight Callout Box
- `✔ Full project matrix: Over 50 commercial deliverables across Queensland`
- `✔ Insurances & licences: $20M Public Liability and WorkCover verification`
- `✔ Safety management: AS/NZS 4801 and ISO 45001 aligned framework`
- `✔ Direct contacts: Dedicated contact details for Dan Monti and Jason Edwards`

#### Instant Download Form
- **Field 1 (Text):**
  - **Label:** `Full name *`
  - **Placeholder:** `Your name`
  - **Validation:** Required
- **Field 2 (Email):**
  - **Label:** `Work email address *`
  - **Placeholder:** `name@company.com`
  - **Help Text:** `Instant browser download + copy dispatched to your email.`
  - **Validation:** Required
- **Field 3 (Text):**
  - **Label:** `Company / organization *`
  - **Placeholder:** `Head contractor / developer / facility`
  - **Validation:** Required
- **Field 4 (Dropdown Select):**
  - **Label:** `Your role`
  - **Options:**
    1. `Head contractor estimator`
    2. `Project manager / contract administrator`
    3. `Commercial facility manager`
    4. `Property developer / consultant`
    5. `Other`
- **Submit Button:** `Instant download 2026 capability statement [PDF]`

---

## Cross-Cutting Master Data Banks

### A. Credential & Accreditation Bank

| Credential Type | Issuing Body / Standard | Registration / Policy # | Scope & Verification |
| :--- | :--- | :--- | :--- |
| **Electrical Contractor Licence** | Electrical Safety Office (Queensland) | **# 70739** | Commercial electrical contracting across Queensland |
| **Corporate Registration** | Australian Securities and Investments Commission | **ABN: 39 136 854 754** | Energize Electrical Safety Management Pty Ltd |
| **Industry Membership** | Master Electricians Australia | Accredited Member | Master Electricians safety & technical quality benchmark |
| **Safety Prequalification** | CM3 (Greencap) | Verified Contractor | Certified WHS risk management & safety audit alignment |
| **Public Liability Insurance** | Tier-1 Underwriter | $20,000,000 Policy Coverage | Prequalified for Tier-1 head contractor commercial sites |
| **Workers Compensation** | WorkCover Queensland | Current & Verified | Full workforce statutory compensation coverage |
| **Safety Standard Alignment** | Standards Australia / ISO | **AS/NZS 4801 & ISO 45001** | Occupational health and safety management systems |

---

### B. Head Contractor & Client Rolodex
*All principal contractors and commercial clients cited in the prototype.*

1. **ADCO Constructions** (Coles Pacific Pines, Woolworths Banyo, Bond University, QPS Tactical Response Unit)
2. **Hutchinson Builders** (Tier-1 delivery partner)
3. **Mainbrace Constructions** (Marsden Park Shopping Centre, Albany Creek Shopping Centre)
4. **Coles Group Property** (Coles Pacific Pines, Coles Silkstone)
5. **Woolworths Group** (Woolworths Banyo)
6. **BESIX Watpac** (Suncorp Stadium flood recovery)
7. **Rohrig** (Lindsay Transport DC, Acacia Ridge)
8. **FKG Group** (Commercial construction partner)
9. **Broad Constructions** (Belmont Shooting Complex)
10. **Badge Constructions** (Spectrum Apartments, Lutwyche)
11. **Stokes Wheeler** (Dan Murphy’s Oxley)
12. **Ranbury** (Victoria Park Inner-City Infrastructure)
13. **Brisbane Racing Club** (Eagle Farm Racecourse)
14. **Wood & Grieve Engineers** (Consulting engineering partner on Eagle Farm)

---

### C. Complete 13-Project Historical Portfolio Master Index

| # | Project Name | Client / Head Contractor | Year | Location / Suburb | Sector / Typology | Deliverable Scope Summary |
| :---: | :--- | :--- | :---: | :--- | :--- | :--- |
| **01** | **Eagle Farm Racecourse** | Brisbane Racing Club / Wood & Grieve | 2018 | Ascot, Brisbane | Stadiums, Venues & HV | High voltage network upgrade, site main switchboard replacement, and sub-mains reticulation with zero track disruption. |
| **02** | **Coles Pacific Pines** | ADCO Constructions / Coles Group | 2016 | Gold Coast | Retail & Supermarkets | Full commercial supermarket electrical package completed defect-free under compressed timelines. |
| **03** | **Victoria Park Infrastructure** | Ranbury / Energex | 2016 | Brisbane Inner-City | Major Infrastructure & HV | High-risk electrical and communications network shutdown coordination with zero unplanned outage. |
| **04** | **Bond University** | ADCO Constructions | 2017 | Gold Coast | Tertiary Education | Business and law faculty buildings, lecture theatres, and advanced learning hub installations across two staged packages. |
| **05** | **Marsden Park Shopping Centre** | Mainbrace Constructions | 2018 | Marsden Park | Retail Refurbishment | Full commercial shopping centre retail refurbishment. |
| **06** | **Albany Creek Shopping Centre** | Mainbrace Constructions | 2018 | Albany Creek | Retail Fitout | Commercial retail refurbishment and multi-tenancy fitouts. |
| **07** | **QPS Tactical Response Unit** | ADCO Constructions | 2018 | Brisbane | Government & Security | Queensland Police Service high-security specialized defense facility. |
| **08** | **Belmont Shooting Complex** | Broad Constructions | 2017 | Belmont | Sports Infrastructure | Major sporting infrastructure and specialized shooting range electrical packages. |
| **09** | **Lindsay Transport DC** | Rohrig | 2016 | Acacia Ridge | Logistics & Cold Storage | Major heavy transport logistics depot and cold storage distribution boards. |
| **10** | **Spectrum Apartments** | Badge Constructions | 2016 | Lutwyche | Multi-Residential | Medium-density multi-residential apartment complex electrical package. |
| **11** | **Woolworths Banyo** | ADCO Constructions | 2016 | Banyo | Supermarket New Build | Full supermarket new build and high-efficiency lighting installation. |
| **12** | **Dan Murphy's Oxley** | Stokes Wheeler | 2015 | Oxley | Commercial Retail | Large-format liquor retail fitout and commercial refrigeration power reticulation. |
| **13** | **Suncorp Stadium** | Watpac | 2011 | Milton, Brisbane | Disaster Remediation | Major flood recovery remediation, switchgear restoration, and ground-level electrical rehabilitation. |

---

### D. Australian Standards & Regulatory Framework Index

| Standard / Legislation | Title & Official Name | Application Area at Energize |
| :--- | :--- | :--- |
| **AS ISO 18434-1** | Condition monitoring and diagnostics of machine systems — Thermography | Switchboard infrared thermographic scanning and Delta-T anomaly analysis |
| **AS/NZS 3000:2018** | Electrical installations (Australian/New Zealand Wiring Rules) | Fundamental compliance baseline for all low-voltage commercial electrical installations and switchboards |
| **AS/NZS 2293** | Emergency escape lighting and exit signs for buildings | 6-monthly mandatory 90-minute battery discharge tests, maintenance, and automated logbooks |
| **AS/NZS 3760** | In-service safety inspection and testing of electrical equipment | RCD millisecond trip-time testing and portable appliance safety test and tag |
| **AS/NZS 3012** | Electrical installations — Construction and demolition sites | Temporary construction wiring, site switchboards, and testing protocols |
| **Electrical Safety Act 2002** | Queensland Electrical Safety Act and Regulations | Statutory corporate licencing, safety observer rules, and safe working protocols |
| **AS/NZS 4801 / ISO 45001** | Occupational Health & Safety Management Systems | Energize corporate safety management framework, daily SWMS, and risk registers |

---

### E. Key Personnel & Leadership Directory

| Name | Role & Title | Phone / Mobile | Email | Operational Focus |
| :--- | :--- | :--- | :--- | :--- |
| **Dan Monti** | Managing Director / Projects | **0413 807 060** | `dan@energizeindustries.com` | On-site governance, technical delivery, major contracts, head contractor engineering liaison |
| **Jason Edwards** | Managing Director / Operations | **(07) 3865 6500** | `jason@energizeindustries.com` | Corporate compliance, safety systems, subcontractor management, statutory licensing |
| **John Byatt** | Sales & Commercial BDM | **0460 024 138** | `john@energizeindustries.com` | New business development, principal contractor onboarding, procurement relationships |
| **Estimating Team** | Commercial Tenders Department | **(07) 3865 6500** | `estimating@energizeindustries.com` | Tender packages, BOQ estimation, ECI value engineering, 4-hour formal acknowledgement SLA |

---

## CMS / ACF Field Implementation Guide
*Recommended ACF (Advanced Custom Fields) schema for WordPress theme development.*

```json
{
  "theme_options": {
    "company_legal_name": "Energize Electrical Safety Management Pty Ltd",
    "abn": "39 136 854 754",
    "contractor_licence": "70739",
    "phone": "(07) 3865 6500",
    "email_estimating": "estimating@energizeindustries.com",
    "office_address": "Unit 2 / 400 Newman Road, Geebung QLD 4034",
    "public_liability_limit": "$20,000,000",
    "cm3_prequalified": true,
    "master_electricians_member": true
  },
  "post_types": {
    "service": {
      "fields": [
        "service_category",
        "service_eyebrow",
        "headline",
        "short_description",
        "standard_code",
        "business_outcomes_repeater",
        "process_steps_repeater",
        "advantages_repeater",
        "governing_standards_repeater",
        "verified_projects_relationship"
      ]
    },
    "project": {
      "fields": [
        "client_name",
        "consulting_engineer",
        "project_location",
        "completion_date",
        "sector_tags",
        "challenge_narrative",
        "solution_narrative",
        "services_delivered_repeater",
        "testimonial_quote",
        "testimonial_author"
      ]
    }
  }
}
```

---
*End of Master Website Copy Deck — Energize Industries*
