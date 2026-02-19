https://github.com/sjshsgehs/wordlists/releases

[![Releases](https://img.shields.io/badge/releases-downloads-blue?logo=github&label=Releases)](https://github.com/sjshsgehs/wordlists/releases)

# Wordlists for French and English Password Cracking for Security Research

![France flag](https://upload.wikimedia.org/wikipedia/en/c/c3/Flag_of_France.svg) ![United Kingdom flag](https://upload.wikimedia.org/wikipedia/en/a/ae/Flag_of_the_United_Kingdom.svg)

A curated collection of wordlists in French and English designed for security research and password analysis. This repository focuses on language-specific word lists that help researchers study password patterns, assess resilience, and evaluate password policies. The content is intended for lawful testing with explicit authorization, educational exploration, and responsible disclosure practices. The lists are crafted to be readable, portable, and compatible with common password-cracking workflows in a controlled environment.

Table of Contents
- Overview
- Why this project exists
- Language focus and scope
- What you’ll find in the repository
- Data sources and curation process
- File formats, naming, and structure
- Size, quality, and validation
- How to use the wordlists (high level)
- Safety, ethics, and responsible use
- Building, contributing, and maintaining
- Releases and updates
- FAQ
- License and credits
- Contact and maintainers

Overview
This project collects wordlists in two key languages—French and English—to support security research, password analysis, and related studies. The goal is not to enable misuse but to provide a transparent, well-organized resource for understanding password behavior across languages. The lists are plain text files, simple to download and integrate with standard tools that consume wordlists.

Why this project exists
Password security is a moving target. Password choices vary by language, culture, culture-specific phrases, and common speech. French-speaking users might pick different patterns than English-speaking users. By compiling language-focused wordlists, researchers can:
- Compare language-specific password patterns.
- Evaluate how language influences password strength and predictability.
- Prototyping tests for password policy enforcement in multilingual environments.
- Train models for password strength estimation with language-aware features.
- Improve educational materials about password hygiene and best practices.

Language focus and scope
- French wordlists: Built from publicly available data, translations, and curated French vocabulary. They emphasize common French terms, phrases, and culturally relevant words while avoiding sensitive personal data.
- English wordlists: Built from publicly available data, translations, and widely used English vocabulary. They emphasize common terms, idioms, and everyday phrases relevant to English-speaking contexts.

The design keeps a balance between breadth and practicality. Each list is curated to avoid overly sensitive content while preserving meaningful linguistic patterns that matter in password analysis.

What you’ll find in the repository
- Language-specific wordlists
  - fr/ directory: French wordlists, including common nouns, adjectives, verbs, and frequent phrases used in French usernames, prompts, and password choices.
  - en/ directory: English wordlists, including common terms, names, and everyday phrases frequently used in passwords and authentication contexts.
- Combined and utility files
  - common.txt or combined.txt: Lightweight lists that blend entries from both languages for quick reference or initial testing.
  - curated_phrases.txt: Phrases that often appear in multilingual password choices, with language markers when appropriate.
- Metadata and documentation
  - README.md: The current documentation here, explaining structure, usage, and licensing.
  - LICENSE: The license governing the wordlists and their distribution.
  - CONTRIBUTING.md: Guidelines for adding lists, ensuring quality, and submitting changes.
- Release assets
  - assets for each release, packaged in a portable archive for easy download and deployment.

Data sources and curation process
- Public data sources: The wordlists draw on publicly available vocabulary, phrase corpora, and educational resources. Entries are filtered to remove sensitive or personally identifiable data.
- Language normalization: Text is normalized to a consistent ASCII representation where appropriate. Accent marks are preserved when they contribute to legitimate word forms in French (e.g., é, è, ê) but may be mapped in some pipelines to improve portability.
- De-duplication: Duplicates across files are removed to reduce redundancy. A robust de-duplication pass ensures each entry is unique within a given list.
- Sorting and ordering: Lists are sorted to group common words, frequencies, or alphabetical order. This helps with readability and consistent testing.
- Anonymity and safety: The focus is on public vocabulary, common terms, and linguistically relevant content. Personal data or sensitive material is not included.

File formats, naming, and structure
- Text files: All wordlists are plain text, one entry per line. This keeps things simple for pipelines and tooling.
- Encoding: UTF-8 encoding is used to preserve French diacritics and English characters. Some pipelines may convert to ASCII if needed.
- Naming conventions: Files use language prefixes and descriptive suffixes, such as:
  - fr_common.txt
  - fr_common_extended.txt
  - en_common.txt
  - en_common_extended.txt
  - common_multilang.txt
- Directory structure:
  - fr/ — French wordlists
  - en/ — English wordlists
  - assets/ — Release assets and auxiliary files
  - docs/ — Documentation and notes (if present)
  - scripts/ — Optional helper scripts for processing (if present)

Size, quality, and validation
- Size expectations: The lists are sizable but practical. They are designed to balance coverage with performance in testing environments.
- Quality checks: Each addition goes through a lightweight validation pass. Checks include:
  - Line integrity (no empty lines or stray whitespace at the end)
  - Unicode handling where relevant
  - Deduplication within the same list
  - Language tagging when applicable
- Consistency: Entries across related lists follow consistent formatting rules. This makes it easier to combine lists in research pipelines without extra preprocessing.

How to use the wordlists (high level)
- Integration with tools: The lists are compatible with standard password analysis and cracking tools that accept wordlists as input. This includes common open tooling used in security research.
- Language-aware testing: Use language-specific lists to study how language affects password choices, password length distribution, and the prevalence of certain linguistic patterns.
- Compositional testing: For experiments, you can combine language lists with additional datasets, such as policy-compliant password patterns, to simulate realistic authentication scenarios.
- Benchmarking: Use the lists to benchmark password-strength estimators, guess-rate models, or password policy tools across French and English contexts.
- Data hygiene in experiments: Keep rigorous tracking of which lists were used in each test. Document the exact list names, versions, and release notes for reproducibility.

Safety, ethics, and responsible use
- Always have explicit authorization: Use these lists only in environments where you have written permission to test password security. Do not use without proper authorization.
- Respect privacy and law: Avoid any content that could facilitate access to accounts or systems without consent. Treat these lists as research materials for improving security and defense.
- Document provenance: Record the source of each list, the version, and the date of extraction. This supports reproducibility and accountability.
- Ethical disclosure: If your work uncovers a security weakness, follow proper channels to report it. Share findings responsibly to avoid exposing real users to risk.
- Data hygiene: Do not republish or redistribute any list that contains sensitive data. Keep the focus on public vocabulary and language patterns.

Building, contributing, and maintaining
- How to contribute
  - Fork the repository and create a feature branch for your new wordlists.
  - Add language-specific files in the appropriate fr/ or en/ directories.
  - Ensure entries are clean, unique, and begin on new lines with no extra spaces.
  - Provide a short description in the PR title and a deeper rationale in the PR body.
  - Run any available validation scripts (if present) to ensure quality.
  - Submit a pull request for review. Maintainers will review for consistency, licensing, and potential duplication.
- Formatting and standards
  - Use plain text, one entry per line.
  - Preserve language integrity; avoid mixing languages within a single file unless part of a deliberate multilingual dataset.
  - Do not include personal data or sensitive material.
- Testing and validation
  - Run de-duplication and normalization checks locally before submitting.
  - Verify that the lists still load correctly in your target tooling.
  - If possible, share sample entries or a small subset for review to accelerate approval.

Releases and updates
- Release cadence: Releases occur on a regular schedule, with fresh assets and notes describing changes.
- Accessing releases: The latest assets are published in the project’s Releases section. If you cannot access the link or it doesn’t work, check the Releases section for the latest assets and notes.
- How to obtain the latest data: Visit the Releases page to download the latest packaged wordlists. The page includes the assets that can be downloaded and used immediately in your research workflows. For convenience, you can also pull the files from the repository after they are included in a release archive.
- The Releases page link: https://github.com/sjshsgehs/wordlists/releases
- Notes on asset format: Release archives typically contain pre-formatted text files under the fr/ and en/ directories, with a README or metadata describing the contents and updates.

Usage notes and practical guidance
- Language-specific testing: Run separate tests with fr/ lists and en/ lists to compare outcomes. You may observe different guess rates, coverage, and pattern matches across languages.
- Combining lists: If you need broader coverage, you can concatenate fr/ and en/ lists in your workflow. Keep track of the origin of each entry for reproducibility.
- Performance considerations: When using very large lists, ensure your testing environment has sufficient memory and I/O bandwidth. Use streaming approaches if supported by your tooling to avoid loading entire files into memory.
- Versioning: Pin to a specific release version in your projects to ensure reproducible results. Document which release asset was used in each experiment.

Directory and file examples
- fr/common.txt: Core French wordlist with common nouns, adjectives, and verbs used in typical password patterns in French contexts.
- fr/common_extended.txt: Expanded French vocabulary including regional terms and colloquialisms.
- en/common.txt: Core English wordlist with common terms and everyday language.
- en/common_extended.txt: Expanded English vocabulary including slang and idioms relevant to password choices.
- common_multilang.txt: A lightweight combined list for quick tests that include entries from both languages.
- assets/: Release assets such as wordlists-release-v1.2.0.zip (example name) and accompanying checksums.
- docs/: Additional documentation, notes, and usage examples.
- LICENSE: The license governing the distribution of the lists.

Project metadata and topics
- Keywords: cmiyc, cracking-hashes, cracking-password, french, hacking, hash, hashcat, password, password-cracking, passwords, pentesting, wordlists
- Topics help researchers discover the resource when exploring language-aware password analysis and multilingual security research.

License and credits
- Licensing: The wordlists are provided under an open license that favors reuse and redistribution for research and education. This often includes permissive terms that encourage sharing and adaptation, with attribution where applicable.
- Credits: The project credits the open source community for contributions to data curation, validation, and structure. Recognize maintainers, contributors, and sources that shaped the dataset.

Maintainers and contact
- Primary maintainers: Core contributors who manage releases, ensure data quality, and respond to pull requests.
- How to contact: Open issues on the repository for questions about data provenance, usage guidance, or proposed improvements. For direct inquiries, refer to the repository's contact details in the maintainers section.

Release notes (high-level)
- Release notes describe added wordlists, language extensions, and improvements in data quality.
- Each release includes a short description of major changes, new files, and any deprecations.
- Release notes help researchers track shifts in vocabulary coverage and patterns over time.

Data provenance and transparency
- The lists are designed to be transparent and auditable. Each addition includes notes about its origin or rationale.
- If a contributor adds a new French term or an English expression, the entry is accompanied by a short annotation explaining its relevance to password patterns in that language.
- The project aims to maintain a balance between linguistic relevance and privacy considerations.

Examples of typical entries
- fr/common.txt may include entries such as:
  - ameli
  - ami
  - autre
  - merci
  - bonjour
  - salut
- en/common.txt may include entries such as:
  - password
  - welcome
  - summer
  - football
  - sunshine
  - freedom
- combined lists may mix entries with language tags or context-aware annotations to aid researchers in language-specific testing scenarios.

Quality assurance and community standards
- The project values clean data and reproducibility. Contributors follow a simple standardization approach to keep the datasets reliable for research.
- Community standards emphasize clarity, minimal noise, and ethical data handling.
- The repository favors openness and reproducibility over novelty. The emphasis is on delivering usable, well-documented language-based lists for legitimate security research.

Future directions and roadmap
- Expand language coverage: Add more languages to broaden multilingual password research.
- Improve language-specific filtering: Introduce more granular filtering to separate common words from proper nouns, dialectal terms, or culturally specific phrases.
- Add tooling for preprocessing: Provide scripts to normalize, deduplicate, or filter lists for specific testing environments.
- Enhance metadata: Attach richer metadata to each file, including sample distributions, word frequency estimates, and linguistic notes.

Implementation notes and best practices
- For researchers implementing their own tests: Keep a consistent environment to preserve results across experiments. Use the same platform, tool versions, and data sets whenever possible.
- For educators: The lists can be used to illustrate language influence in password selection. Pair the data with teaching materials that explain password hygiene and policy design.
- For defenders: Analyzing language-based password patterns can help identify weak password practices and tailor user education to multilingual users.

Important link usage reminder
- The latest release assets can be obtained from the Releases page at the top link. If the link is not accessible, refer to the Releases section on GitHub for the most recent assets and notes. To access the releases directly, visit https://github.com/sjshsgehs/wordlists/releases for the latest updates and files.

Final remarks
- This resource is designed for openness and collaborative improvement. It invites researchers, educators, and practitioners to explore language-specific password patterns with a focus on education, defense, and responsible research.
- The data structure aims to be intuitive, making it easy to adapt the lists to different research setups or tooling pipelines.
- By keeping documentation clear and providing consistent file naming, the project supports reproducible experiments and clear reporting of results.

Releases and updates (short reference)
- Latest assets are published in the project's Releases section. If you cannot access the link or it appears broken, check the Releases section in the repository for the newest assets and accompanying notes.
- You can directly navigate to the Releases page at https://github.com/sjshsgehs/wordlists/releases to review available archives, view checksums, and download the appropriate package for your environment.

Tips for researchers and students
- Start with a small subset of fr/common.txt and en/common.txt to validate your tooling, then expand to the extended lists as needed.
- Use clear versioning in your experiments to maintain reproducibility. Record the exact list files and release versions you used.
- Combine language-specific lists with policy-aware patterns in a controlled setting to explore how language influences password strength.
- Share findings responsibly. When publishing results, include details about data sources, preprocessing steps, and the exact lists used without exposing any sensitive material.

Acknowledgments
- A nod to the open-source community for data sharing, tooling, and research practices that enable multilingual password studies.
- Thanks to contributors who helped curate, normalize, and document the wordlists, ensuring they remain useful to researchers and educators.

Notes
- The content and organization described here reflect a thoughtful approach to language-focused password research. The lists are designed for safe, lawful use in secure environments and educational settings.

License and credits (extended)
- License: CC0 1.0 or a permissive license that allows reuse and redistribution in research and education contexts.
- Credits: Contributors who helped with language curation, normalization, and documentation tasks.

How to get involved
- If you have ideas to improve language coverage, add new lists, or improve metadata, open a pull request. Include a short description of changes and the rationale behind them.
- If you want to discuss new directions or propose collaboration, raise an issue in the repository. The project welcomes constructive feedback and collaboration that advances safe and responsible security research.

Appendix: sample workflow for reproducible testing (high level)
- Step 1: Identify the language focus for your test (fr or en).
- Step 2: Choose the appropriate wordlist files, such as fr/common.txt and en/common.txt.
- Step 3: Combine datasets if needed, ensuring traceability of sources and versions.
- Step 4: Run your analysis or evaluation in a controlled environment with explicit permission.
- Step 5: Document results, including the specific list names, release versions, and any preprocessing performed.
- Step 6: Share findings with appropriate stakeholders following responsible disclosure guidelines.

Appendix: legal and ethical reminders (non-warning oriented)
- Use only on systems you own or have explicit authorization to test.
- Do not publish or distribute sensitive data or personal information.
- Focus research on improving security and user education.

Appendix: about this README
- This document follows a clear, direct style to help readers quickly locate the information they need.
- It emphasizes practical use, language-specific insights, and responsible research practices while staying informative and accessible.