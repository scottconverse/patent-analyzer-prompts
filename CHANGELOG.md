# Changelog

All notable changes to Patent Analyzer Prompts will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0] - 2026-04-01

### Changed
- All 6 stage prompts now position the AI as an "AI-powered research assistant" rather than a "patent attorney" or "patent strategist"
- Every stage output now begins with a mandatory disclaimer identifying the output as AI-generated research, not legal advice
- Section titles softened to reflect landscape analysis rather than legal directives:
  - "File or Don't File" is now "Filing Landscape Assessment"
  - "Bottom-Line Recommendation" is now "Overall Landscape Assessment"
  - "Examiner Rejection Simulation" is now "Common Examiner Concerns in This Technology Area"
  - "Freedom-to-Operate Flag" is now "Potential Blocking IP to Discuss with Counsel"
- Assessment labels updated:
  - "FILE NOW" is now "LANDSCAPE FAVORS FILING"
  - "DO NOT FILE" is now "SIGNIFICANT OBSTACLES IDENTIFIED"
  - "DOCUMENT MORE" is now "MORE DOCUMENTATION WOULD STRENGTHEN POSITION"
  - "DESIGN PATENT ONLY" is now "DESIGN PATENT AVENUE WORTH EXPLORING"
- Stage 3 now uses Research Findings / Analysis Notes structure to separate factual observations from interpretive analysis
- Conclusions now include scope qualifiers acknowledging search limitations
- Stage 6 closing disclaimer expanded to explicitly state tool author and AI are not lawyers

### Added
- Mandatory disclaimer block in common rules, output at the start of every stage
- Per-stage disclaimer anchors ensuring disclaimers survive copy-paste between conversations
- Active hedging language in Stages 3, 5, and 6 conclusions
- Fact/judgment boundary markers in Stage 3 patentability analysis
- LEGAL_NOTICE.md with comprehensive 5-section legal notice
- Section 5.5 (AI Limitations) in Terms of Service

### Changed
- License changed from MIT to Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)
- CC BY-SA 4.0 includes UPL disclaimer retention clause requiring derivative works to preserve all legal disclaimers
- Terms of Service updated to reflect new license, section titles, and AI limitation disclosures

## [1.1.0] - 2026-03-15

### Added
- Web search fallback warnings in Stage 2
- URL verification for prior art references
- Prior art verification gate in Stage 3
- Legal reference caveats for training-data-only references
- Cost estimate date stamps with USPTO fee verification links
- Minimum 50-word input threshold in Stage 1
- Truncation safeguards in Stages 3-5
- Word count targets for consistent output

### Fixed
- Web search language aligned in Stage 4 (changed from "requires" to "benefits from")

## [1.0.0] - 2026-02-01

### Added
- Initial release: 6-stage patent landscape analysis prompt system
- Stages: Technical Intake, Prior Art Search, Patentability Analysis, Deep Dive, IP Strategy, Final Report
- Handoff block system for multi-conversation workflow
- Common rules for consistent output formatting
- Support for Claude Pro/Max/Team and Gemini Advanced
