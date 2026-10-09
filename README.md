<h1 align="center">aSc Timetables Patcher</h1>

<p align="center">An executable patcher and manifest generator for aSc Timetables.</p>
<p align="center"><strong>Rust · Windows · JSON</strong></p>

---

### Patcher

Verifies the source file's SHA-256 hash and applies changes defined in a JSON manifest. Locates target bytes using patterns or file offsets, checks them against the expected values, and replaces them. Saves the result to the original file or a separate output file.

Adds startup code to the executable that fills in missing school and username values in the Windows registry while preserving existing values.

### Manifest Generator

Generates byte patterns with `??` wildcards for known patch offsets. Accounts for x86/x64 instructions, relative addresses, and relocations, then verifies that each pattern is unique and remains valid as patches are applied in sequence. Saves the updated JSON manifest to a new file.
