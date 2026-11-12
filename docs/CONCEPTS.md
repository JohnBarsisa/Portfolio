# Product Concepts — User Journeys & Proposed Architecture

This catalogue expands the visual boards in the [main portfolio](../README.md). **All workflows below describe product intent and design concepts unless an implementation is explicitly linked.** Visuals are mockups, not proof of deployed services, compliance or live integrations.

## CONPAY — Consumer and merchant payments

[Brand board](showcase/conpay.jpg) · [Device and architecture board](showcase/conpay-detail.jpg)

**Users:** customers, merchants, payments operations.  
**Proposed journey:** customer launches mobile wallet → merchant creates a payable request or compatible contactless session → an authorised PSP handles tokenised authorisation → both sides receive confirmed state → merchant dashboard reconciles payments.  
**Key design requirements:** backend-managed idempotency, webhooks, reconciliation, RBAC, audit events, and tokenisation. No financial institution affiliation, card-processing certification or real-money deployment is claimed. [CONPAY source concept](https://github.com/JohnBarsisa/CONPAY) is currently private.

## MANNA — Bible & Notes

[Brand board](showcase/manna.jpg) · [Architecture board](showcase/manna-architecture.jpg)

**Users:** readers and personal-study users.  
**Flow:** choose a Bible book and translation → read chapters → select verses → highlight, bookmark or write notes → adjust reading font/theme → resume from locally saved position.  
**Current code:** Expo Router + React Native + TypeScript with local state, tests and Bible source datasets in a private repo. **Future only:** cloud sync and licensed commercial translations. Preview art is not a release build.

## ROVA — Interstate mobility marketplace

[Workflow board](showcase/rova.jpg) · [Architecture board](showcase/rova-architecture.jpg)

**Four roles:** passenger, driver, transport-operator manager, central ROVA administrator.  
**Proposed journey:** passenger searches routes → compares operators and departures → chooses a seat → pays or reserves through approved options → receives a trip reference → driver begins an assigned journey → passenger follows permitted GPS updates → operator manages fleet and reconciliation.  
**Controls:** operator separation, verified payments, secure GPS permissions, incident escalation and audited admin overrides. No live booking inventory, transport affiliation or production GPS feed is implied.

## GateWise — Estate access and security

[Responsive product board](showcase/gatewise.jpg) · [System architecture](showcase/gatewise-architecture.jpg)

**Roles:** residents, gate/security staff, estate managers.  
**Proposed journey:** resident issues a visitor pass → visitor presents code/pass at entry → gate checks validity and restrictions → arrival is recorded → staff and resident can review the activity log.  
**Potential integrations:** access cards, optional CCTV/intercom, multi-device apps and event notifications. Hardware integrations and cloud services shown in the visual are design targets unless separately implemented.

## KEKS — Local keke transport

[Brand/product board](showcase/keks.jpg) · [System architecture](showcase/keks-architecture.jpg)

**Roles:** riders, drivers and fleet/operations staff.  
**Proposed journey:** rider chooses pickup and destination → available driver accepts → trip and status updates are shared → trip completes with a recorded fare/settlement → support handles disputes.  
**Design focus:** yellow/black Keke-inspired identity, shared cross-platform UI, route visibility and clear driver-state transitions.

## NairaPay / NPay — Payments interface

[Consumer/merchant board](showcase/nairapay.jpg) · [System architecture](showcase/nairapay-architecture.jpg)

**Proposed journey:** create a secure account → select payment, transfer or merchant operation → verify request → receive settlement/status response from approved providers → see history and notifications.  
**Requirements:** provider licensing, KYC/AML responsibilities, fraud monitoring, key security and reconciliation. These are concepts and requirements, not live banking functions.

## Fashion Brew — Lifestyle commerce

[Brand + app + architecture board](showcase/fashion-brew.jpg)

**Customer journey:** browse apparel for children/adults, accessories, perfumes and cosmetics → filter products → view variants and sizes → add to cart → complete checkout → track order status.  
**Merchant journey:** manage catalogue, stock, orders, promotions and fulfilment.  
**Scope:** product concept and broad lifestyle brand, not a claim of active e-commerce infrastructure.

## Eleeshas — Ice-cream brand experience

[Brand and commerce concept](showcase/eleeshas.jpg)

**Proposed journey:** explore flavours and bundles → customise or order products → select fulfilment → receive updates. A staff interface could manage offers and order queues.  
**Scope:** visual consumer/operations workflows, not a proven ordering backend.

## PDF Forge — PDF utility

[Desktop product concept](showcase/pdf-forge.jpg)

**Proposed journey:** select PDFs → choose a tool such as merge, split, compress, convert, annotate or organise → preview the outcome → export to a chosen location.  
**Engineering considerations:** protect local file privacy, preserve originals, handle malformed documents, and clearly separate supported from planned transformations. The image does not establish completed functionality.

## Unzipper — Archive utility

[Desktop product concept](showcase/unzipper.jpg)

**Proposed journey:** drag in a local archive → inspect contents → choose extraction destination/options → extract with progress and error feedback → organise output files.  
**Security considerations:** archive traversal/path sanitisation, decompression-bomb guards and safe overwrite behaviour. The mockup is not a published installer.

## ZOVYRA — Premium media experience

[Brand/product board](showcase/zovyra.jpg) · [Secondary experience board](showcase/zovyra-detail.jpg)

**Proposed journey:** import or discover owned/licensed media → browse a visually rich library → play in responsive desktop/mobile views → manage queues and preferences.  
**Scope:** branding/product direction. Do not conflate this concept automatically with the separate MediaFlow downloader repository.

## Aurora Player — Media-player direction

[Primary design](showcase/aurora-player.jpg) · [Feature/UI board](showcase/aurora-player-detail.jpg)

**Proposed journey:** organise a media library → inspect cover/metadata → play audio or video → manage queues and format preferences.  
**Scope:** alternative player design; release code, codec coverage and third-party integrations are not established by the concept images.

---

## Technical/product principles

1. Share one clear design system across iOS, Android, tablet and web; vary only necessary platform controls.
2. Put account and business validation on the backend; do not rely on client-side checks for trust decisions.
3. Require permissions and audit records for financial, health, location and access-control operations.
4. Present demonstrations with synthetic data, never production clients' information.
5. Separate **working implementation**, **prototype** and **concept** in every public description.

**Presentation reference:** the MeridianFlow pages in the source artwork are used only as layout inspiration, not represented here as a personal product.
