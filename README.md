# Narrative Physics Engine

AI-powered system for generating complete 40-chapter psychological domestic thrillers.

## Features
- Automated story generation from premise to complete manuscript
- 40-chapter structure mapped to 8-sequence thriller framework
- Modular library of reusable elements (200+ items planned)
- Flexible POV system (single/dual, first/third person)
- Custom or library-generated settings
- Hybrid selection mode (AI random + user choice)
- Automated midpoint and final reviews
- Built-in humanization pass

## Quick Start
1. Configure preferences in `config/narrative-physics-config.yaml`
2. Run `python scripts/generate-premise.py --mode auto --count 3`
3. Select premise from options
4. System auto-generates complete 40-chapter manuscript
5. Review final output in `books/[book-name]/manuscript/`

## Structure
- **config/**: System configuration files
- **templates/**: Story structure templates
- **library/**: Reusable story elements
  - `character-archetypes/`: 20 protagonist and antagonist archetypes
  - `trope-library/`: 20+ tropes across psychological, thriller, domestic, and twist categories
  - `plot-modules/`: Reusable plot patterns
  - `setting-elements/`: Location and atmosphere options
  - `relationship-dynamics/`: Relationship patterns
  - `secrets-and-lies/`: Secret types
  - `psychological-patterns/`: Psychological elements
- **books/**: Generated book projects
- **scripts/**: Automation workflow scripts
- **docs/**: System documentation

## Workflow
1. **Premise generation** (3-5 options)
2. **Story bible construction** - Full 40-chapter structure
3. **Chapter drafting** (2-3 chapter batches)
4. **Midpoint review** (Chapter 20) - Automated consistency check
5. **Continue drafting** (Chapters 21-40)
6. **Final review** - Comprehensive manuscript review
7. **Humanization pass** - Remove AI tells, add variation
8. **User review** (acquisition editor mode)

## Library System
Modular elements across multiple categories:
- **Character archetypes**: 20 types (10 protagonists, 10 antagonists)
- **Trope library**: 20+ tropes across multiple categories
- **Plot modules**: Reusable story patterns
- **Setting elements**: Location and atmosphere options

### Current Library Contents
- ✅ 10 Protagonist archetypes (anxious-everywoman, gaslighted-spouse, overprotective-parent, unreliable-trauma-survivor, desperate-social-climber, new-mother, trophy-wife, caregiver-burnt-out, perfectionist-unraveling, isolated-expat, widow-starting-over)
- ✅ 10 Antagonist archetypes (charming-manipulator, calculated-sociopath, desperate-protector, wounded-avenger, parasitic-friend, envious-rival, controlling-matriarch, predatory-mentor, obsessive-stalker, hidden-psychopath)
- ✅ 20 Tropes across psychological, thriller, domestic, betrayal, identity, power-dynamic, twist, and misdirection categories

## Selection Modes
- **Auto**: AI randomly selects all elements from library
- **Manual**: User chooses all elements
- **Hybrid**: User specifies some, AI fills rest with compatible elements

## Output
Each generated book includes:
- 40-chapter manuscript (markdown)
- Story bible
- Story state tracker
- Character profiles
- Clue/payoff tracker
- Revision history

## Genre Focus
Psychological domestic thrillers featuring:
- Marriages, families, neighbors
- Secrets, lies, manipulation
- Gaslighting and paranoia
- Power dynamics and betrayal
- "Who can I trust?" tension
- Contemporary or recent past settings

## Automation Scripts

### generate-premise.py
Generates 3-5 story premise options using selected library elements.
```bash
python scripts/generate-premise.py --mode auto --count 3
# or
python scripts/generate-premise.py --mode manual --selections selections.json
# or
python scripts/generate-premise.py --mode hybrid --selections partial-selections.json
```

### build-story-bible.py
Constructs complete story infrastructure from selected premise.
```bash
python scripts/build-story-bible.py
```

### draft-chapters.py
Drafts chapters in batches of 2-3 with proper POV voice.
```bash
python scripts/draft-chapters.py --book-path books/my-book --batch-size 3
```

### update-story-state.py
Updates story-state-tracker.md after each chapter batch.
```bash
python scripts/update-story-state.py --book-path books/my-book --chapters 1,2,3
```

### midpoint-review.py
Automated review at Chapter 20 with revisions.
```bash
python scripts/midpoint-review.py --book-path books/my-book
```

### final-review.py
Comprehensive review of complete 40-chapter manuscript.
```bash
python scripts/final-review.py --book-path books/my-book
```

### humanization-pass.py
Removes AI tells and adds human variation.
```bash
python scripts/humanization-pass.py --book-path books/my-book
```

## Configuration

### POV System
Configure in `config/pov-system-config.yaml`:
- Single POV (40 chapters, one character)
- Dual POV with ratios: 70/30, 65/35, or 60/40
- Voice options: first person, third limited, third close

### Sequence Structure
8 sequences mapped to 40 chapters:
1. **Seq 1 (Ch 1-5)**: Normal / Calm Before Storm (10-20% tension)
2. **Seq 2 (Ch 6-10)**: Inciting Unease (20-35% tension)
3. **Seq 3 (Ch 11-15)**: Denial / Maintain Normalcy (35-45% tension)
4. **Seq 4 (Ch 16-20)**: Growing Pressure → **MIDPOINT TWIST #1** (45-60% tension)
5. **Seq 5 (Ch 21-25)**: Crisis / Midpoint Shift (60-75% tension)
6. **Seq 6 (Ch 26-30)**: Descent into Chaos (75-85% tension)
7. **Seq 7 (Ch 31-37)**: Climax → **ACT III REVEAL (TWIST #2)** (85-100% tension)
8. **Seq 8 (Ch 38-40)**: Aftermath → **Optional EPILOGUE STING (TWIST #3)** (falling action)

## Requirements
- Python 3.8+
- PyYAML
- Additional dependencies for AI generation (TBD based on implementation)

## Project Status
This is a foundational structure for an AI-powered novel generation system. Core components are in place:
- ✅ Configuration system
- ✅ Template system
- ✅ Library foundation (40 character archetypes, 20 tropes)
- ✅ Automation workflow scripts
- 🚧 Additional library content (ongoing expansion)
- ⏳ AI integration layer (planned)

## Future Enhancements
- Expand library to 200+ elements
- Integrate with AI models for generation
- Add web interface
- Export to multiple formats (DOCX, EPUB)
- Advanced customization options
- Collaborative editing features

## Contributing
This is a specialized creative writing system. Contributions to the library (new character archetypes, tropes, plot modules) are welcome following the established template structure.

## License
[License TBD]

## Support
For questions or issues, please open an issue in this repository.

---

**Created for generating standalone 40-chapter psychological domestic thrillers with automated planning, drafting, and revision.**
