# Tabletop Game Creation: Role & Specialization Map
*Research notes for AI agent persona development*
*Domain: Board games, card games, puzzle games, escape rooms, TTRPGs*
*Date: 2026-05-24*

---

## How to Read This Document

Each role entry covers:
- **Produces**: The concrete deliverables this role owns
- **Works in**: Tools, formats, and file types they operate in
- **Distinct because**: What separates this role from adjacent ones
- **Overlaps with**: Roles that share skill surface area or are commonly combined

Overlap notes at the end of each section identify natural consolidation points for AI personas.

---

## Section 1: Creative / Design Roles

---

### 1.1 Game Designer (Core Mechanics)

**Produces:**
- Game concept documents (elevator pitch, high concept, design pillars)
- Mechanics specification documents (rules drafts, edge case registers)
- Prototype specifications (component lists, card counts, player count ranges)
- Iterative design logs documenting mechanical changes between versions
- Player experience goals document (what players should feel at turn 3, at game end)

**Works in:**
- Google Docs / Word (design docs)
- Spreadsheets (math models, balance matrices, card frequency tables, probability calculations)
- Tabletop Simulator or Tabletopia (digital prototyping)
- Physical prototyping (printed index cards, poker chips, tokens)
- Notion or Obsidian (design wikis for complex games)

**Distinct because:**
The core game designer works at the level of systems and loops — what actions exist, what resources exist, how they interact, how the game ends, what creates meaningful decisions. They are concerned with elegance, fairness, pacing, and the arc of the play experience. They are not primarily concerned with story (narrative designer), visual presentation (art roles), or writing (rulebook writer), though they must communicate with all of them.

**Overlaps with:**
- TTRPG System Designer (for system-level mechanics work)
- Puzzle Designer (for puzzle-heavy games)
- Balance Reviewer (game designers often do early balance work before a dedicated reviewer takes over)

---

### 1.2 Puzzle Designer

**Produces:**
- Individual puzzle specifications (setup, solution path, intended difficulty rating)
- Puzzle flow maps (sequence dependencies, branching paths)
- Puzzle logic documents (the constraints, the aha moment, the intended reasoning chain)
- Hint systems and tiered hint scripts
- Blind testing notes and difficulty calibration logs

**Works in:**
- Spreadsheets (dependency mapping, difficulty scoring matrices)
- Diagrams and flowcharts (Figma, Miro, Lucidchart) for puzzle flow
- Word processors for puzzle text and hint writing
- Physical prototypes (paper, props, physical locks for escape rooms)
- Puzzle-specific tools like CrosswordCompiler, Crossword Nexus, or custom constraint solvers

**Distinct because:**
Puzzle designers work at the level of a single challenge — a cipher, a lock mechanism, a riddle, a logic grid, a hidden message. Their craft is the aha moment: the gap between apparent impossibility and sudden clarity. They obsess over whether the solution path is discoverable, whether the puzzle is fair (no arbitrary leaps), and whether difficulty is calibrated correctly.

**Overlaps with:**
- Escape Room Designer (heavily — escape room design is substantially puzzle design)
- Narrative Designer (puzzles in narrative games must integrate with story logic)
- Rules Clarity Tester (puzzle wording clarity is a shared concern)

---

### 1.3 Narrative Designer

**Produces:**
- World bible / setting document (history, factions, geography, tone)
- Narrative arc documents (how story develops across sessions or plays)
- Event card flavor and consequence writing integrated into mechanics
- Branching dialogue trees or outcome tables
- Lore integration specs (what the player learns when, how mechanics reinforce theme)
- Character profiles and faction relationships

**Works in:**
- Twine or Ink (branching narrative tools, especially for digital or hybrid games)
- World Anvil or Notion (worldbuilding databases)
- Google Docs / Word (prose and script writing)
- Spreadsheets (event tables, encounter tables, branching outcome matrices)
- Campaign tools like Airtable for managing large narrative content volumes

**Distinct because:**
Narrative designers sit at the intersection of mechanics and story. They are not simply writing flavor text — they are ensuring that what a player does mechanically feels thematically coherent. They differ from an adventure module writer in that they work on integrated game systems rather than pre-written scenarios.

**Overlaps with:**
- Flavor Text Writer
- TTRPG Adventure/Module Writer
- Game Designer (in heavily thematic games)
- Campaign Setting Designer

---

### 1.4 TTRPG System Designer

**Produces:**
- Core mechanic specification (dice resolution system, attribute system, action economy)
- Character creation rules and advancement system
- Conflict resolution rules (combat, social, exploration procedures)
- GM/facilitator guidance on running the system
- Subsystem designs (crafting, downtime, chase mechanics, etc.)
- Playtesting packets for system validation

**Works in:**
- Word processors (rules documents, system drafts)
- Spreadsheets (probability modeling for dice pools, balance across character options)
- Affinity Publisher or InDesign (for layout-ready draft documents)
- Foundry VTT or Roll20 (testing system compatibility with VTT automation)
- AnyDice (dice probability calculator)

**Distinct because:**
TTRPG system designers are building a toolkit that a GM and players will use to generate emergent stories — not a fixed experience. The deliverable is a procedure engine, not a product with a defined win state. They must account for the human GM as a component of the system.

**Overlaps with:**
- Game Designer (shared mechanics thinking, probability modeling)
- Adventure Module Writer (system designers often write the first published adventure)
- Campaign Setting Designer

---

### 1.5 Escape Room Designer

**Produces:**
- Room flow document (the sequence of puzzles and narrative reveals)
- GM/host guide (how staff run the room, reset procedures, hint management)
- Physical prop specifications (what needs to be built, sourced, or fabricated)
- Narrative script (the story context players receive and uncover)
- Reset checklists and maintenance documentation
- Difficulty tuning notes based on playtest data

**Works in:**
- CAD or SketchUp (physical room layout)
- Figma or physical whiteboards (puzzle flow diagrams)
- Word processors (narrative scripts, GM guides)
- Spreadsheets (prop inventory, puzzle timing data)
- Physical fabrication (props, printed materials, physical locks, electronics)

**Distinct because:**
Escape room designers work with physical space as a design medium. They must account for group dynamics in a shared physical environment, reset logistics, ADA accessibility of physical props, and the presence of a live GM/host.

**Overlaps with:**
- Puzzle Designer (very heavily)
- Narrative Designer
- Manufacturing Spec Writer (for prop fabrication specifications)

---

### 1.6 Card Game Designer

**Produces:**
- Card set specification (card types, costs, effects, keyword glossary)
- Economy and resource system design
- Archetype and synergy maps (what strategies should be viable)
- Draft/sealed format specifications
- Expansion design briefs

**Works in:**
- Spreadsheets (card databases, set statistics, mana curve analysis, keyword frequency)
- Nanodeck or Card Creator (rapid card prototyping)
- MSE (Magic Set Editor) for card templating
- Python or R for statistical analysis of card balance
- Tabletop Simulator for digital playtesting

**Distinct because:**
Card games have a unique design challenge around card pool interactions at scale. A card game designer must think combinatorially — a single new card interacts with every other card in the pool. They must manage templating rigor, set architecture, and the metagame.

**Overlaps with:**
- Game Designer (at the system level)
- Balance Reviewer
- Rules Clarity Tester

---

## Section 2: Art & Visual Roles

---

### 2.1 Card Layout Artist

**Produces:**
- Card template files (master layout in Affinity Publisher, InDesign, or Photoshop)
- Production-ready card print files (CMYK, bleeds, correct DPI — typically 300-800 DPI)
- Card back and front alignment guides
- Variable data card sheets (cards with unique text/images in repeated template)
- Font licensing documentation for print

**Works in:**
- Adobe InDesign (primary for professional production)
- Affinity Publisher (popular indie alternative)
- Adobe Illustrator (for vector elements, icons, frames)
- Photoshop (for image placement and raster elements)
- Data merge workflows for bulk card production
- The Game Crafter, DriveThruCards, or MakePlayingCards template systems

**Distinct because:**
Card layout is a specialized print production discipline. Cards have extreme constraints: tiny physical footprint (typically 63mm x 88mm poker size), must remain readable at arm's length, must render correctly in print (CMYK color gamut, not RGB). The layout artist must know bleed, safe zones, spot UV limitations, linen finish impacts on color.

---

### 2.2 Component Designer

**Produces:**
- Token artwork (player tokens, resource cubes, victory point markers)
- Tile artwork and die-cut specifications
- Player board layout and iconography
- Rulebook spot illustrations and diagram figures
- Icon/symbol system with usage guide
- 3D component specifications (meeples, miniatures) for manufacturer

**Works in:**
- Adobe Illustrator (vector-first for tokens and icons)
- Affinity Designer (vector alternative)
- Photoshop (for textured or painted component looks)
- Blender or ZBrush (for 3D component renders or sculpt files)
- Manufacturer-specific die-cut templates

**Distinct because:**
Components must function physically — a token must be punched cleanly from a board, visible at table distance, and identifiable by color-blind players. Component designers think about physical manufacturing constraints as much as aesthetics.

---

### 2.3 Box / Packaging Designer

**Produces:**
- Box lid and bottom artwork (dieline-based layout)
- Box back copy layout
- Insert/tray design specification
- Shrink wrap, sleeve, or band design
- Retail shelf impact mockups
- Print-ready dieline files for manufacturer

**Works in:**
- Adobe Illustrator and InDesign (dieline-based layout is vector-first)
- Affinity Publisher/Designer
- Manufacturer-provided dieline templates (Panda GM, Longpack, Ludo Fact)
- Mockup tools (Smartmockups, Placeit) for presentation

**Distinct because:**
Box design is retail-first. The box lid must sell the game from across a game store aisle. The dieline requires precise structural knowledge (tuck box vs. two-piece box, insert tolerances, lid-to-bottom clearances). Publishers often hire specifically for this because it is a retail marketing asset as much as a production file.

---

### 2.4 Board / Map Artist

**Produces:**
- Game board artwork (modular tiles or fixed board)
- Regional maps for TTRPG or narrative games
- Visual hierarchy design for the playing surface
- Annotated production files (layer organization for printing)

**Works in:**
- Photoshop (for painted board art, textured surfaces)
- Illustrator (for clean graphic map elements)
- Procreate (for illustrated hand-drawn style maps)
- Affinity Publisher (for final layout and print file assembly)
- Campaign Cartographer 3+ (for TTRPG map production)
- Inkarnate, Wonderdraft, Dungeondraft (TTRPG community mapping tools)

**Distinct because:**
Board art must solve a functional design problem: the playing surface is a UI. Players need to read game state, place components accurately, and navigate the board without confusion. The board artist must understand the game mechanics to know what information needs to be visually dominant.

---

### 2.5 Icon / Symbol Designer

**Produces:**
- Icon library (action icons, resource icons, keyword icons, faction icons)
- Icon usage style guide (size minimums, color rules, context restrictions)
- Accessibility annotations (color-blind safe palettes, shape differentiation)
- Icon SVG/AI source files for use across all components

**Works in:**
- Adobe Illustrator (vector-first)
- Affinity Designer
- Figma (increasingly common for icon systems)
- Color accessibility tools (Colour Contrast Analyzer, Coblis color blind simulator)

**Distinct because:**
Icon design is a system design problem, not an illustration problem. Icons must form a coherent language with consistent visual metaphors, predictable stylistic grammar, reliable legibility at tiny sizes. A player seeing an icon for the first time should be able to guess its meaning from context.

---

### 2.6 Illustration Art Director

**Produces:**
- Art brief document for each illustration (scene description, mood, color palette, reference images)
- Style guide (visual consistency rules across all game art)
- Artist sourcing and contracting documentation
- Art review notes and revision requests
- Final art asset inventory with approved files organized for production handoff

**Works in:**
- Google Drive or Dropbox (asset management)
- Notion or Airtable (art tracker — status per illustration, per artist)
- Slack or email (artist communication)
- Photoshop (for art review and comp mockups)

**Distinct because:**
The art director does not make art — they orchestrate it. They translate game design intent into visual direction, manage multiple artists simultaneously, enforce style consistency, and ensure all art is production-ready.

---

### 2.7 Print-and-Play Layout Designer

**Produces:**
- PnP PDF with printer-friendly layouts (grayscale option, ink-saving option, cut lines)
- Tabletop-distance-readable card and board designs
- Assembly instruction pages
- A4 and Letter format versions
- Component checklist and materials list pages

**Works in:**
- Affinity Publisher or InDesign (layout)
- Illustrator / Affinity Designer (component art)
- Photoshop (image optimization for screen and home printing)
- PDF export workflows with embedded fonts

**Distinct because:**
PnP design is constrained by home printer reality: 8.5x11 or A4 page, inkjet or laser output, imprecise hand-cutting. Components must be larger and more tolerant of cutting error. Color must read well on both color and greyscale printers.

---

## Section 3: Writing Roles

---

### 3.1 Rulebook Writer

**Produces:**
- Complete rulebook manuscript (learn-to-play and reference rulebook)
- Quick start guide or reference card text
- FAQ / errata document
- Rules index
- Turn structure summary text
- Annotated example-of-play section

**Works in:**
- Google Docs / Word (drafting and collaborative editing)
- Affinity Publisher or InDesign (final layout, working with the layout artist)
- Version control or change tracking for rules revisions

**Distinct because:**
Rulebook writing is technical writing with a specific constraint: the reader must be able to reconstruct a complete, accurate mental model of the game from the text alone, in a single read, without prior context. This requires sequencing information in learning order (not importance order), anticipating every ambiguity, and writing with surgical precision.

---

### 3.2 Flavor Text Writer

**Produces:**
- Card flavor text (typically 1-3 sentences per card, in-universe voice)
- Event card narrative descriptions
- Item/equipment lore entries
- Chapter or section epigraphs in rulebooks
- In-world documents, journals, letters embedded in game materials

**Works in:**
- Google Docs / Word
- The game's established world bible
- Style guides and voice documents
- Spreadsheets (card-by-card flavor text tracker)

**Distinct because:**
Flavor text writing requires extreme economy of language and total submission to voice. Word count constraints are severe (often under 20 words on a card) while requiring emotional resonance, world-building, and thematic reinforcement. The mechanical function comes first; the flavor is an enhancement.

---

### 3.3 Kickstarter Campaign Writer

**Produces:**
- Campaign page copy (hero section, game description, why back this, stretch goals text)
- Update posts (during and after campaign)
- Backer reward tier descriptions
- FAQ section
- Risk and challenges section (Kickstarter required)
- Referral and share messaging

**Works in:**
- Kickstarter campaign editor
- Google Docs (drafts before publishing)
- Backerkit or Gamefound (for pledge manager copy)

**Distinct because:**
Kickstarter copy is sales copy with a community dimension. It must convert skeptical strangers into financial backers within minutes. Unlike traditional marketing copy, it must also manage risk transparency (backers are investors, not customers) and communicate production credibility.

---

### 3.4 Marketing Copywriter

**Produces:**
- Press kit copy (game description, feature bullets, quote-ready taglines)
- Social media post copy (platform-adapted)
- Email newsletter copy
- Ad copy (Facebook/Instagram/Reddit ads)
- Box back copy
- Convention/demo table signage copy

**Works in:**
- Google Docs / Word
- Social media schedulers (Buffer, Hootsuite, Later)
- Mailchimp or Klaviyo (for email)
- Meta Ads Manager / Reddit Ads

---

### 3.5 Press Kit Writer

**Produces:**
- Press kit document (game overview, spec sheet, key features, target audience, media contact)
- Reviewer pitch email templates
- Influencer outreach copy
- Review copy request response templates
- Award submission copy

**Works in:**
- Google Docs / Word
- PDF layout tools (Affinity Publisher / Canva for designed press kit PDFs)

---

### 3.6 TTRPG Adventure / Module Writer

**Produces:**
- Adventure manuscript (complete scenario with hooks, scenes, NPCs, encounters, resolution)
- Encounter stat blocks
- NPC profiles (personality, motivations, secrets, read-aloud text)
- Area/location descriptions (boxed read-aloud text + GM notes)
- Adventure flowchart / scene map
- Handouts (player-facing documents embedded in the adventure)

**Works in:**
- Google Docs / Word (drafting)
- Affinity Publisher or InDesign (for layout-ready manuscript)
- The game's specific SRD for rules compliance
- Homebrewery or GM Binder (community layout tools)
- World Anvil (for interconnected setting content)

**Distinct because:**
Module writing is structured creative writing with strict functional requirements. Every scene must give the GM enough information to improvise around player choices. The writer must write in two registers simultaneously: evocative prose for read-aloud text, and efficient, scannable reference text for GM notes.

---

### 3.7 Scenario Writer (Board Game / Escape Room)

**Produces:**
- Scenario book entries (setup instructions, win/loss conditions, special rules)
- Campaign chapter scripts
- Legacy game narrative envelopes and reveal scripts
- Escape room narrative frame documents
- Boss encounter scripts

---

## Section 4: Playtesting & QA Roles

---

### 4.1 Blind Playtester Coordinator

**Produces:**
- Blind playtest recruitment materials (brief, instructions, NDA)
- Blind playtest packet (rules, components, feedback form — no author present)
- Aggregated blind playtest report
- Confusion map (where in rules players got stuck, by frequency)
- Net Promoter Score or comparable summary metric

**Works in:**
- Google Forms / Typeform (feedback collection)
- Google Docs (playtest packet assembly)
- Spreadsheets (response aggregation and analysis)
- The Game Crafter or print services (for producing playtest copies)

---

### 4.2 Playtest Log Analyst

**Produces:**
- Session log (game state at key moments, decisions made, outcomes)
- Win/loss rate by player count, faction, starting position
- Turn length and session length data
- Problematic interaction log (edge cases encountered during play)
- Trend analysis across multiple sessions

**Works in:**
- Spreadsheets (primary tool — data entry, pivot tables, charts)
- Google Forms (for structured in-session data capture)
- Statistical tools (R, Python with pandas) for larger data sets

---

### 4.3 Balance Reviewer

**Produces:**
- Balance assessment report (which strategies, factions, or cards are over/under-powered)
- Probability analysis (dice outcomes, card draw frequencies, resource curve analysis)
- Recommended adjustment list with rationale
- Pre/post-adjustment comparison analysis

**Works in:**
- Spreadsheets (probability modeling, win rate tracking)
- Python or R (for complex simulations or large card pools)
- AnyDice (dice probability calculator — industry-standard free tool)

---

### 4.4 Rules Clarity Tester

**Produces:**
- Rules ambiguity report (specific passages that caused confusion, with test subject quotes)
- Edge case registry (situations the current rules don't clearly resolve)
- Suggested rewrite options for ambiguous passages
- Rules comprehension quiz

---

### 4.5 Accessibility Reviewer

**Produces:**
- Accessibility audit report (color contrast, color-blind legibility, cognitive load, physical handling)
- Specific remediation recommendations with before/after examples
- Accessibility features documentation (for press kit and game description)
- Alternative component recommendations (larger text editions, colorblind variant files)

**Works in:**
- Color contrast analyzers (WebAIM contrast checker, Colour Contrast Analyzer)
- Color blindness simulators (Coblis, Sim Daltonism)
- Physical prototype handling (testing components for dexterity requirements)

---

## Section 5: Production / Manufacturing Roles

---

### 5.1 Print Production Researcher

**Key manufacturers covered:**
- The Game Crafter (US, on-demand, low MOQ, good for prototyping and small runs)
- DriveThruCards / DTRPG (on-demand, card and book focus, TTRPG market)
- MakePlayingCards (US/Hong Kong, playing card specialist, reasonable MOQ)
- Panda Game Manufacturing (China, industry standard for mid/large Kickstarters, 1500+ MOQ)
- Longpack Games (China, competitive pricing, similar to Panda)
- Ludo Fact (Germany, premium European manufacturing)
- Cartamundi (Belgium/global, playing card specialist at scale)
- Shuffled Ink (US, playing card and trading card specialist)
- PrintNinja (China, broader print products including game boxes and books)

**Produces:**
- Manufacturer comparison report (capabilities, MOQs, lead times, pricing, quality tiers)
- Sample order plan and evaluation criteria
- Preferred vendor shortlist with rationale
- Timeline from file submission to delivery (by manufacturer)

---

### 5.2 Component Cost Estimator

**Produces:**
- Bill of materials (complete component list with unit counts)
- Per-unit manufacturing cost estimate (at various quantities)
- COGS model including manufacturing, shipping, duties, and fulfillment
- Break-even analysis (what retail price or Kickstarter funding level is required)
- Sensitivity analysis (how costs change at 500, 1000, 2000, 5000 unit quantities)

**Works in:**
- Spreadsheets (primary tool — complex multi-variable cost models)
- Manufacturer quoting tools (Panda GM online quote tool, Longpack quote sheets)
- Freight forwarder rate tools (for shipping cost estimation)
- Fulfillment provider rate cards (Quartermaster Logistics, Spiral Galaxy, etc.)

---

### 5.3 Manufacturing Spec Writer

**Produces:**
- Complete manufacturing specification document (per-component material specs, dimensions, color specs, finish specs)
- Dieline specifications for custom components
- Proof review checklist and approval criteria
- Component QC acceptance criteria

---

### 5.4 File Prep for Print (Prepress Specialist)

**Produces:**
- Production-ready print files (correct color profile, DPI, bleed, safe zone, file format per manufacturer)
- File preflight report (confirming all specs are met)
- Color-separated files (if spot color or spot UV is involved)
- Manufacturer submission package

**Works in:**
- Adobe Acrobat (PDF preflight)
- Affinity Publisher / InDesign (for file adjustments)
- Photoshop (for raster image correction and color profile conversion)
- Preflight tools (PitStop for Acrobat, built-in preflight in InDesign)

---

## Section 6: Digital / Asset Creation Roles

---

### 6.1 Tabletop Simulator Mod Creator

**Produces:**
- TTS workshop mod (published playable game in Tabletop Simulator)
- Scripted automation (Lua scripts for card dealing, token management, turn tracking, rules enforcement)
- Asset files (card face images, board images, token images, bag organization)
- Custom component models (3D objects for unique components)
- Mod documentation for players

**Works in:**
- Tabletop Simulator (Unity-based, built-in scripting environment)
- Lua (TTS scripting language)
- Atom or VS Code (for Lua script editing with TTS extensions)
- Photoshop / Affinity (for asset image preparation)

---

### 6.2 Print & Play PDF Designer

**Produces:**
- PnP PDF with printer-friendly layouts (grayscale option, ink-saving option, cut lines)
- Layered PDF (allowing players to toggle ink-saving options)
- Interactive PDF (fillable fields for trackers, click-through rules links)
- Digital-first variant (screen-optimized version for tablet play without printing)

---

### 6.3 Digital Rulebook Formatter

**Produces:**
- Bookmarked, searchable PDF rulebook (hyperlinked index, section bookmarks)
- Screen-optimized layout (two-page spread vs. single-page scroll variants)
- Accessible PDF (tagged for screen readers, alt text for diagrams)
- EPUB version (for e-reader distribution, where applicable)
- Online rules reference (hosted on publisher website)

---

## Section 7: Community / Publishing Roles

---

### 7.1 Kickstarter Campaign Strategist

**Produces:**
- Campaign structure plan (funding goal, stretch goal ladder, tier structure, timing)
- Pre-launch timeline (mailing list growth plan, preview campaign, launch day checklist)
- Stretch goal design
- Backer communication calendar
- Post-campaign fulfillment update schedule
- Campaign analytics review

**Works in:**
- Kickstarter Creator Dashboard
- Backerkit or Gamefound (pledge manager platforms)
- Mailchimp / ConvertKit (pre-launch mailing list)

---

### 7.2 BoardGameGeek (BGG) Community Manager

**Produces:**
- BGG game listing (complete, accurate, with all editions, expansions, and components listed)
- BGG forum presence (answering rules questions, engaging with reviews)
- BGG GeekList and promo posts
- Review seeding and reviewer relationship management

**Works in:**
- BoardGameGeek website (BGG forums, image manager, game entry editor)
- BGG Publisher Tools
- Discord (for community hub)

---

### 7.3 Publisher Pitch Writer

**Produces:**
- Publisher pitch document
- Sell sheet (one-page visual pitch document — the standard format for publisher pitching)
- Pitch email templates
- Publisher target list and research notes
- Convention pitch preparation materials

---

### 7.4 Retail Sales Sheet Writer

**Produces:**
- Retail sell sheet (distributor/retailer-facing one-pager with wholesale pricing, case pack, product specs)
- MSRP and distributor margin structure documentation
- Product catalog copy
- Trade show booth materials copy

---

## Section 8: TTRPG-Specific Roles

---

### 8.1 Campaign Setting Designer

**Produces:**
- World bible (geography, history, factions, cultures, cosmology)
- Gazetteer (location-by-location reference, usable by GMs)
- Timeline of world events
- Faction relationship map
- Player-facing lore document (what players know vs. GM secrets)
- Random tables specific to the setting

**Works in:**
- World Anvil (world building platform, industry standard)
- Notion or Obsidian (interconnected notes)
- Dungeondraft / Inkarnate (regional and world maps)
- Affinity Publisher / InDesign (for layout-ready gazetteers)

---

### 8.2 One-Shot Designer

**Produces:**
- Self-contained adventure playable in a single 3-4 hour session
- Pregenerated characters
- Condensed GM guide (all information needed on 1-2 reference pages)
- Convention-ready package (minimal setup time, supports rotating GM/players)

---

### 8.3 Safety Tools Integration Specialist

**Produces:**
- Safety tools documentation embedded in the module or system (Lines and Veils, X-Card, Script Change)
- Content warning list
- Session zero guide
- Calibration guidance

**Distinct because:**
Safety tools integration emerged from TTRPG culture as the medium addressed consent, trauma, and player wellbeing more seriously. Requires knowledge of established frameworks (Johanna Koljonen's work, Beau Jágr Sheldon's work, the RPG Safety Toolkit). No direct equivalent in board game design.

---

### 8.4 VTT (Virtual Tabletop) Prep Specialist

**Produces:**
- Foundry VTT module (scene setup, actor sheets, journal entries, macros, lighting, sound)
- Roll20 campaign setup (maps, tokens, character sheets, rollable tables)
- Token artwork files (top-down tokens for NPCs, PCs, monsters)
- Dynamic lighting maps (with walls and doors configured)
- Sound design cues and ambient playlists
- System-specific automation scripts

**Works in:**
- Foundry VTT (JavaScript API, JSON module structure)
- Roll20 (HTML/CSS/JavaScript API)
- Dungeondraft (for map creation optimized for VTT light engine)
- Token editors (Token Stamp 2, Tokenizer for Foundry)
- VS Code (for scripting)

---

### 8.5 Custom RPG System Designer

Additional distinct deliverables for fully bespoke systems:
- System Reference Document (SRD) — the open license version of the core rules
- Open Game License (OGL) or Creative Commons licensing documentation
- Designer's notes / design manifesto
- System compatibility guide

---

## Section 9: Role Overlap Map and Consolidation Guide

*Natural consolidation clusters for AI persona design*

### Cluster A: Core Game Design
**Roles**: Game Designer + Card Game Designer + Balance Reviewer
**Consolidation logic**: All three require systems thinking, probability modeling, and mechanical iteration.

### Cluster B: Puzzle & Escape Room Design
**Roles**: Puzzle Designer + Escape Room Designer + Scenario Writer
**Consolidation logic**: All three work at the individual challenge level and require puzzle-design thinking.

### Cluster C: Card & Component Visual Production
**Roles**: Card Layout Artist + Component Designer + Icon/Symbol Designer + PnP Layout Designer
**Consolidation logic**: All four use the same tools (Illustrator, InDesign/Affinity Publisher) and the same print production knowledge.

### Cluster D: Campaign & Marketing Writing
**Roles**: Kickstarter Campaign Writer + Marketing Copywriter + Press Kit Writer
**Consolidation logic**: All three produce externally-facing promotional prose and share the same game description asset.

### Cluster E: Manufacturing Pipeline
**Roles**: Print Production Researcher + Component Cost Estimator + Manufacturing Spec Writer + File Prep for Print
**Consolidation logic**: Sequential pipeline — each step's output feeds the next. A single "Production Specialist" persona can manage the full chain.

### Cluster F: TTRPG Writing
**Roles**: Adventure Module Writer + One-Shot Designer + Scenario Writer + Flavor Text Writer
**Consolidation logic**: All four produce structured creative writing within a defined game system.

### Cluster G: Digital Adaptation
**Roles**: Tabletop Simulator Mod Creator + VTT Prep Specialist + Digital Rulebook Formatter + PnP PDF Designer
**Consolidation logic**: All four produce digital access versions of physical game content.
**Note**: TTS and VTT require real Lua/JavaScript scripting — keep separate if that's a core need.

### Cluster H: Playtesting & QA
**Roles**: Blind Playtester Coordinator + Playtest Log Analyst + Rules Clarity Tester + Accessibility Reviewer
**Consolidation logic**: All four are QA roles focused on the player experience.

---

## Section 10: Format Specificity Table

| Role | Board Game | Card Game | Puzzle Game | Escape Room | TTRPG |
|---|---|---|---|---|---|
| Game Designer | Core | Core | Core | Core | Core |
| Puzzle Designer | Optional | Rare | Core | Core | Optional |
| Narrative Designer | Optional | Optional | Rare | Optional | Core |
| TTRPG System Designer | No | No | No | No | Core |
| Escape Room Designer | No | No | No | Core | No |
| Card Layout Artist | Common | Core | Rare | No | Common |
| Board/Map Artist | Core | Rare | Common | No | Core |
| Rulebook Writer | Core | Core | Optional | Rare | Core |
| Scenario Writer | Common | Rare | Optional | Common | Core |
| Adventure Module Writer | No | No | No | No | Core |
| Safety Tools Specialist | No | No | No | No | Core |
| VTT Prep Specialist | No | No | No | No | Core |
| TTS Mod Creator | Common | Common | No | No | Optional |
| BGG Community Manager | Core | Core | Optional | No | Common |
| One-Shot Designer | No | No | No | No | Core |
| Campaign Setting Designer | No | No | No | No | Core |

---

## Section 11: Tool Ecosystem Summary

| Tool | Primary Roles |
|---|---|
| Adobe InDesign / Affinity Publisher | Card Layout, PnP Layout, Box Design, Rulebook Layout, Module Layout |
| Adobe Illustrator / Affinity Designer | Component Design, Icon Design, Box Design, Board Art |
| Adobe Photoshop / Affinity Photo | Board Art, Card Layout, Asset Prep, TTS Assets |
| Google Docs / Word | All writing roles |
| Google Sheets / Excel | Balance Review, Cost Estimation, Playtest Analysis, Card Database |
| AnyDice | Balance Review, TTRPG System Design |
| Tabletop Simulator | Game Design, Card Game Design, TTS Mod Creator |
| Foundry VTT | TTRPG System Design, VTT Prep Specialist |
| Roll20 | TTRPG System Design, VTT Prep Specialist |
| World Anvil | Narrative Design, Campaign Setting Design, Adventure Module |
| Dungeondraft / Inkarnate | Board/Map Art, VTT Prep, Campaign Setting Design |
| Lua / JavaScript | TTS Mod Creator, VTT Prep Specialist |
| Python / R | Balance Review, Playtest Log Analysis |
| Kickstarter / Backerkit | Campaign Strategist, Campaign Writer |
| Homebrewery / GM Binder | Adventure Module Writer, One-Shot Designer |
| Figma | Icon Design, Puzzle Flow Diagrams, Escape Room Design |
| Twine / Ink | Narrative Design, Adventure Module |
| AnyDice | Balance Review, TTRPG System Design |
| MSE (Magic Set Editor) | Card Game Design |

---

*39 distinct roles identified across 8 domains. 8 natural consolidation clusters identified for AI persona design.*
