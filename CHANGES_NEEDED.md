# Required Changes to KiCad Project

## Purpose
This document outlines the specific changes that need to be made to the KiCad project files to address issues discovered during the purple stepper motor driver assembly process.

---

## Schematic Changes

### 1. Stepper Motor Driver Update
**File:** `*.kicad_sch` (main schematic)

**Changes Required:**
- [ ] Replace red stepper driver symbol with purple driver symbol
- [ ] Update component reference (e.g., U1, U2, etc.)
- [ ] Verify pin numbering and functionality
- [ ] Update component value/part number
- [ ] Check and update power pins (VCC, GND, motor power)
- [ ] Verify control signal pins (STEP, DIR, ENABLE)

**Purple Driver Specifications to Verify:**
```
- Operating Voltage: [TO BE DETERMINED]
- Logic Voltage: [TO BE DETERMINED]
- Maximum Current: [TO BE DETERMINED]
- Microstepping: [TO BE DETERMINED]
- Package Type: [TO BE DETERMINED]
```

### 2. Power Supply Section
**Changes Required:**
- [ ] Verify LDO component can handle purple driver current requirements
- [ ] Check input/output capacitor values
- [ ] Verify voltage ratings of all power supply components
- [ ] Update power supply schematic notes

### 3. Decoupling Capacitors
**Changes Required:**
- [ ] Verify decoupling capacitor values near stepper drivers
- [ ] Check capacitor voltage ratings
- [ ] Ensure adequate bulk capacitance for motor current spikes
- [ ] Add additional capacitors if needed

---

## PCB Layout Changes

### 1. Footprint Updates
**File:** `*.kicad_pcb`

**Changes Required:**
- [ ] Verify stepper driver footprint matches purple driver package
- [ ] Check pad sizes and shapes
- [ ] Verify hole sizes for through-hole components
- [ ] Update footprint library references

### 2. Power Trace Width
**Changes Required:**
- [ ] Calculate required trace width for motor current
- [ ] Measure existing power trace widths
- [ ] Widen traces if necessary to handle current safely
- [ ] Verify ground plane adequacy

**Trace Width Calculations:**
```
For [X] Amps current:
- Minimum trace width (1oz copper): [TO BE CALCULATED]
- Recommended trace width with margin: [TO BE CALCULATED]
- Current trace width: [TO BE MEASURED]
```

### 3. Thermal Management
**Changes Required:**
- [ ] Add thermal vias under stepper drivers if needed
- [ ] Verify copper pour areas for heat dissipation
- [ ] Check clearances for airflow
- [ ] Consider heatsink mounting if required

### 4. Silkscreen Updates
**Changes Required:**
- [ ] Add "Purple Driver" marking or version identifier
- [ ] Update component values on silkscreen
- [ ] Add polarity markings for motor connections
- [ ] Add assembly notes if space permits
- [ ] Update revision number/date

---

## Bill of Materials (BOM) Updates

### Changes Required:
- [ ] Update stepper driver part number to purple driver
- [ ] Verify all passive component values
- [ ] Update manufacturer part numbers
- [ ] Add alternative part numbers if available
- [ ] Update supplier information
- [ ] Verify current ratings of all components

**BOM Format:**
```
Reference | Description | Part Number | Manufacturer | Quantity | Notes
---------|-------------|-------------|--------------|----------|------
U1,U2    | Purple Stepper Driver | [PART_NUMBER] | [MANUFACTURER] | 2 | [SPECIFICATIONS]
```

---

## Library Updates

### 1. Symbol Library
**File:** `*.kicad_sym`

**Changes Required:**
- [ ] Create or update purple stepper driver symbol
- [ ] Verify pin names and numbers
- [ ] Add datasheet reference
- [ ] Update component description
- [ ] Add relevant specifications as properties

### 2. Footprint Library
**File:** `*.kicad_mod`

**Changes Required:**
- [ ] Create or update purple driver footprint
- [ ] Verify pad dimensions from datasheet
- [ ] Add proper 3D model association
- [ ] Add courtyard and fabrication layers
- [ ] Update footprint description

### 3. 3D Models
**Changes Required:**
- [ ] Add or update 3D model for purple driver
- [ ] Verify component heights and clearances
- [ ] Update assembly visualization

---

## Design Rules Check (DRC) Updates

### Changes to Verify:
- [ ] Run DRC after making changes
- [ ] Check for clearance violations
- [ ] Verify track width rules
- [ ] Check hole sizes
- [ ] Verify component placement

---

## Testing and Validation

### Pre-Fabrication Checks:
- [ ] ERC (Electrical Rules Check) passes
- [ ] DRC (Design Rules Check) passes
- [ ] Visual inspection of PCB layout
- [ ] Cross-reference with purple driver datasheet
- [ ] Verify BOM against schematic
- [ ] Check Gerber files before ordering

### Post-Assembly Tests:
- [ ] Continuity testing
- [ ] Power supply voltage measurements
- [ ] Driver functionality test
- [ ] Thermal testing under load
- [ ] Full system integration test

---

## Documentation Updates

### Files to Update:
- [ ] README.md - Add notes about driver type
- [ ] Assembly instructions
- [ ] User manual
- [ ] Schematic PDF export
- [ ] Manufacturing notes
- [ ] Test procedures

---

## Version Control

### Recommended Versioning:
- **Current Version:** 1.0 (with red drivers - assumed)
- **New Version:** 1.1 (with purple drivers)

### Version Marking Locations:
- [ ] PCB silkscreen
- [ ] Schematic title block
- [ ] Assembly documentation
- [ ] Git repository tags

---

## Dependencies and Prerequisites

Before making changes, ensure you have:
- [ ] Purple stepper driver datasheet
- [ ] Actual measurements from assembled boards
- [ ] Access to KiCad project files
- [ ] Backup of current design
- [ ] Component specifications from suppliers

---

## Change Implementation Plan

1. **Preparation Phase** (Day 1)
   - Gather all datasheets and specifications
   - Take measurements from assembled boards
   - Create backup of current design

2. **Schematic Updates** (Day 2)
   - Update driver symbols
   - Verify power supply design
   - Run ERC

3. **Layout Updates** (Day 3)
   - Update footprints
   - Check trace widths
   - Update silkscreen

4. **Verification Phase** (Day 4)
   - Run DRC
   - Generate Gerbers
   - Review all changes

5. **Documentation Phase** (Day 5)
   - Update all documentation
   - Generate manufacturing files
   - Create release notes

---

## Risk Assessment

### High Risk Items:
- ⚠️ Footprint incompatibility could require board redesign
- ⚠️ Insufficient power trace width could cause failure
- ⚠️ Inadequate thermal design could damage components

### Mitigation Strategies:
- Verify all specifications before ordering new boards
- Review changes with experienced hardware engineer
- Order small batch for testing before production run

---

## Notes

- All changes should be reviewed and approved before fabrication
- Consider creating separate design branch for purple driver variant
- Maintain compatibility with existing firmware if possible
- Document any component substitutions clearly

---

## Related Documents
- [KICAD_ISSUES.md](./KICAD_ISSUES.md) - Detailed issue tracking
- [ASSEMBLY_NOTES.md](./ASSEMBLY_NOTES.md) - Assembly procedures and notes

## Last Updated
2026-02-07
