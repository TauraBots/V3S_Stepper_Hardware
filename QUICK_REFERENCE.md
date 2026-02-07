# Quick Reference Guide - Purple Driver Issues

## 🎯 Purpose
Fast reference for anyone working with V3S Stepper Hardware boards using purple stepper motor drivers.

---

## 📚 Document Navigation

| Document | Purpose | When to Use |
|----------|---------|-------------|
| [README.md](./README.md) | Project overview and getting started | First time working with project |
| [KICAD_ISSUES.md](./KICAD_ISSUES.md) | Comprehensive issue tracking | Want to see all known issues |
| [CHANGES_NEEDED.md](./CHANGES_NEEDED.md) | Required KiCad modifications | Planning KiCad project updates |
| [ASSEMBLY_NOTES.md](./ASSEMBLY_NOTES.md) | Assembly procedures and tips | Before/during board assembly |
| [ISSUE_TEMPLATE.md](./ISSUE_TEMPLATE.md) | Template for documenting new issues | Found a new issue to report |

---

## ⚡ Quick Start

### Before Assembly
1. Read [ASSEMBLY_NOTES.md](./ASSEMBLY_NOTES.md) sections 1-3
2. Check [KICAD_ISSUES.md](./KICAD_ISSUES.md) for known issues
3. Gather required tools and materials
4. Prepare ESD-safe workspace

### During Assembly
1. Follow assembly sequence in ASSEMBLY_NOTES.md
2. Pay special attention to purple driver orientation
3. Verify all component values against BOM
4. Perform visual inspection after each step

### After Assembly
1. Run all quality checks from ASSEMBLY_NOTES.md
2. Perform electrical testing before powering on
3. Document any issues found using ISSUE_TEMPLATE.md
4. Report problems in GitHub Issues

### If Updating KiCad Project
1. Review [CHANGES_NEEDED.md](./CHANGES_NEEDED.md)
2. Verify purple driver datasheet specifications
3. Make changes systematically (schematic → layout → BOM)
4. Run ERC and DRC checks
5. Update version numbers
6. Document all changes

---

## 🔍 Known Critical Issues

### Issue Priority Matrix

| Priority | Description | Action Required |
|----------|-------------|-----------------|
| 🔴 **CRITICAL** | Stepper driver compatibility | Verify footprint and specifications |
| 🔴 **CRITICAL** | Power trace width | Check current capacity |
| 🟡 **MEDIUM** | Component markings | Verify orientation during assembly |
| 🟡 **MEDIUM** | LDO specifications | Confirm current rating adequate |

### Top 3 Things to Check

1. **Purple Driver Footprint**
   - Verify pins align with pads
   - Check pin 1 orientation marking
   - Ensure full seating of component

2. **Power Supply**
   - Measure input voltage before connecting drivers
   - Verify LDO output voltage
   - Check for shorts between power and ground

3. **Solder Joints**
   - Inspect all driver pins for good solder joints
   - Check for bridges between adjacent pins
   - Verify no cold joints (dull appearance)

---

## 🛠️ Troubleshooting Quick Reference

### Board Won't Power On
```
Check: Power connection → Polarity → Shorts → LDO → Fuses
```

### Driver Not Working
```
Check: Orientation → Power → Solder joints → Enable pin → Logic signals
```

### Excessive Heat
```
Check: Short circuits → Current settings → Thermal connections → Ventilation
```

### Intermittent Behavior
```
Check: Cold solder joints → Loose connections → Component values → Signal integrity
```

---

## 📋 Assembly Checklist

Quick checklist for assembling one board:

### Pre-Assembly
- [ ] Review documentation
- [ ] Verify BOM components match requirements
- [ ] Check purple driver part number
- [ ] Prepare workspace with ESD protection
- [ ] Gather tools and materials

### SMD Components (30-45 min)
- [ ] Apply solder paste (if using reflow)
- [ ] Place resistors
- [ ] Place capacitors
- [ ] Place ICs
- [ ] Reflow or hand solder
- [ ] Inspect joints

### LDO (5-10 min)
- [ ] Verify part number
- [ ] Check orientation
- [ ] Solder with adequate heat on thermal pad
- [ ] Inspect connections

### Through-Hole (20-30 min)
- [ ] Install connectors
- [ ] Install purple stepper drivers (verify orientation!)
- [ ] Install terminal blocks
- [ ] Install remaining components
- [ ] Trim leads
- [ ] Clean flux

### Testing (15-20 min)
- [ ] Visual inspection (100% coverage)
- [ ] Check for shorts (power to ground)
- [ ] Verify continuity on power rails
- [ ] Initial power-on with current limit
- [ ] Measure regulated voltages
- [ ] Functional test with motors

### Documentation (5 min)
- [ ] Record assembly date
- [ ] Note any issues or deviations
- [ ] Test results recorded
- [ ] Serial number assigned (if applicable)

**Total Time:** ~1.5-2 hours per board

---

## 📞 Getting Help

### Found a New Issue?
1. Check if it's already documented in [KICAD_ISSUES.md](./KICAD_ISSUES.md)
2. Use [ISSUE_TEMPLATE.md](./ISSUE_TEMPLATE.md) to document it
3. Open a GitHub issue with details and photos
4. Reference Issue #2 (Purple Driver Assembly)

### Need Clarification?
- Comment on GitHub Issue #2
- Review related documentation sections
- Check external datasheets and references

### Making Changes?
- Create a branch from `main`
- Update relevant documentation
- Test changes thoroughly
- Submit pull request with clear description

---

## 🔗 External Resources

### Datasheets Needed
- [ ] Purple stepper motor driver datasheet
- [ ] LDO voltage regulator datasheet
- [ ] PCB substrate specifications
- [ ] Motor specifications

### Standards and Guidelines
- IPC-A-610: Acceptability of Electronic Assemblies
- IPC-J-STD-001: Requirements for Soldered Electrical and Electronic Assemblies
- KiCad documentation and best practices
- Motor control application notes

---

## 📊 Status Dashboard

### Current Project Status
- **KiCad Project:** ⏳ Pending upload (Issue #1)
- **Purple Driver Documentation:** ✅ Complete
- **Assembly Testing:** 🔄 In Progress (Issue #2)
- **Required Changes:** 📋 Identified and documented

### Documentation Status
- ✅ Issue tracking document created
- ✅ Changes needed document created
- ✅ Assembly notes completed
- ✅ README updated
- ✅ Quick reference guide created

### Next Steps
1. Complete assembly of boards with purple drivers (Issue #2)
2. Document specific issues found
3. Upload KiCad project files (Issue #1)
4. Implement required changes based on findings
5. Test revised boards

---

## 🔄 Update Frequency

This is a **living document** that should be updated:
- After each assembly session
- When new issues are discovered
- When changes are made to KiCad project
- When testing reveals new information

**Last Updated:** 2026-02-07

---

## 📝 Key Terms

- **Purple Drivers:** Stepper motor drivers with purple PCB (model TBD)
- **Red Drivers:** Original stepper motor drivers (predecessor to purple)
- **V3S:** Version 3 Stepper robot platform
- **LDO:** Linear Dropout voltage regulator
- **SMD:** Surface Mount Device
- **ESD:** Electrostatic Discharge
- **BOM:** Bill of Materials
- **ERC:** Electrical Rules Check (KiCad)
- **DRC:** Design Rules Check (KiCad)

---

## ✨ Tips and Tricks

### Assembly Tips
- **Use magnification** for SMD components - it makes a huge difference
- **Test incrementally** - don't wait until everything is soldered
- **Double-check orientation** before soldering - easier than rework
- **Clean flux residue** for better inspection and reliability
- **Document as you go** - don't rely on memory later

### KiCad Tips
- **Back up before changes** - keep original design safe
- **Use version control** - commit frequently with clear messages
- **Run checks often** - catch issues early with ERC/DRC
- **Update libraries** - keep component libraries current
- **Document changes** - update title block and version info

### Testing Tips
- **Start low and slow** - use current-limited power supply
- **Measure before powering** - check for shorts first
- **Heat means problem** - hot components indicate issues
- **Trust your senses** - burning smell or noise = stop immediately
- **Keep notes** - record all test results and observations

---

**For detailed information, always refer to the full documentation files.**

**Questions?** Open an issue on GitHub or comment on Issue #2.
