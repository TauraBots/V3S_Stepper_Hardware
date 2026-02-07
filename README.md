# V3S_Stepper_Hardware

Kicad project repository for the stepper v3s robot pcb

## Overview

This repository contains the KiCad hardware design files for the V3S Stepper robot PCB. The board is designed to control stepper motors using compatible stepper motor drivers.

## Current Status

⚠️ **Important:** The repository is being updated to document issues found during assembly with **purple stepper motor drivers** (see Issue #2).

## Documentation

### 📚 Navigation
- **[DOCUMENTATION_INDEX.md](./DOCUMENTATION_INDEX.md)** - Complete guide to all documentation (start here!)
- **[QUICK_REFERENCE.md](./QUICK_REFERENCE.md)** - Fast reference guide for working with purple driver boards

### Assembly and Issues
- **[KICAD_ISSUES.md](./KICAD_ISSUES.md)** - Comprehensive tracking of issues discovered during purple driver assembly
- **[CHANGES_NEEDED.md](./CHANGES_NEEDED.md)** - Detailed list of required changes to the KiCad project
- **[ASSEMBLY_NOTES.md](./ASSEMBLY_NOTES.md)** - Assembly procedures, best practices, and troubleshooting
- **[ISSUE_TEMPLATE.md](./ISSUE_TEMPLATE.md)** - Template for documenting new issues

### Related Issues
- [Issue #1: Init commit](https://github.com/TauraBots/V3S_Stepper_Hardware/issues/1) - Add KiCad hardware project with BOM
- [Issue #2: Electronics with purple driver Assembly](https://github.com/TauraBots/V3S_Stepper_Hardware/issues/2) - Assembly task tracking

## Repository Structure

```
V3S_Stepper_Hardware/
├── README.md              # This file - start here
├── DOCUMENTATION_INDEX.md # Complete guide to all docs
├── QUICK_REFERENCE.md     # Fast reference guide
├── KICAD_ISSUES.md       # Issue tracking for KiCad project
├── CHANGES_NEEDED.md     # Required changes documentation
├── ASSEMBLY_NOTES.md     # Assembly procedures and notes
├── ISSUE_TEMPLATE.md     # Template for documenting issues
└── [KiCad project files to be added per Issue #1]
```

## Stepper Motor Driver Compatibility

### Purple Drivers (Current Focus)
The board is being documented and potentially revised for compatibility with **purple stepper motor drivers**. See documentation for details on:
- Known issues
- Required changes
- Assembly notes
- Testing procedures

### Red Drivers (Original Design)
The board was originally designed for red stepper motor drivers. If using the original design, refer to the initial specifications.

## Getting Started

### Prerequisites
- KiCad 7.0 or later (version to be confirmed)
- Access to purple stepper motor driver datasheets
- Soldering equipment and tools (see ASSEMBLY_NOTES.md)

### Building the Hardware

1. **Review Documentation**
   - Read [KICAD_ISSUES.md](./KICAD_ISSUES.md) for known issues
   - Review [CHANGES_NEEDED.md](./CHANGES_NEEDED.md) for any pending updates
   - Study [ASSEMBLY_NOTES.md](./ASSEMBLY_NOTES.md) before assembly

2. **PCB Fabrication**
   - [To be added: Gerber files and manufacturing notes]

3. **Component Procurement**
   - [To be added: BOM with part numbers]

4. **Assembly**
   - Follow assembly sequence in ASSEMBLY_NOTES.md
   - Use proper ESD protection
   - Perform all quality checks

5. **Testing**
   - Follow testing procedures in documentation
   - Document any issues found

## Contributing

Contributions are welcome! If you find issues during assembly or testing:

1. Check existing documentation to see if the issue is already known
2. Open a new issue with detailed description and photos if applicable
3. Update relevant documentation files
4. Submit pull request with improvements

## Support

For questions or issues:
- Open an issue on GitHub
- Reference relevant documentation files
- Include detailed description and photos when applicable

## License

[License to be added]

## Authors and Acknowledgments

- **icarusMQ** - Initial design and assembly testing
- See contributor list for additional contributors

## Version History

- **v1.0** - Initial design (red drivers) - Status: In development
- **v1.1** - Purple drivers variant - Status: Documentation phase

---

**Last Updated:** 2026-02-07
