# Assembly Notes - V3S Stepper Hardware with Purple Drivers

## Overview
This document provides assembly notes, lessons learned, and best practices for assembling the V3S robot boards with purple stepper motor drivers.

**Reference:** Issue #2 - Electronics with purple driver Assembly

---

## Assembly Sequence

### 1. Small SMD Components
**Order of Assembly:**
1. Resistors (smallest first)
2. Capacitors (smallest first)
3. Diodes and LEDs
4. ICs and integrated circuits

**Best Practices:**
- Use magnification for small components
- Apply solder paste evenly
- Use stencil if available for consistent application
- Verify component orientation before reflow
- Check polarity markings carefully

**Common Issues:**
- Tombstoning (component standing on one end)
- Component shifting during reflow
- Incorrect polarity on polarized components
- Solder bridges between pads

**Solutions:**
- Apply even heat during reflow
- Use proper solder paste amount
- Double-check orientation before heating
- Use solder wick or braid to remove bridges

---

### 2. LDO (Linear Dropout Regulator)
**Assembly Notes:**
- Verify part number before soldering
- Check thermal pad requirements
- Ensure adequate solder on thermal pad for heat dissipation
- Verify input/output pin identification

**Critical Checks:**
- Orientation (tab position)
- Pin alignment
- Thermal connection to PCB
- Solder joints quality

**Testing:**
- Measure input voltage
- Measure output voltage (should match specification)
- Check for excessive heat during operation
- Verify current capacity

---

### 3. Through-Hole Components
**Assembly Order:**
1. Connectors (lowest profile first)
2. Stepper motor drivers (if through-hole)
3. Terminal blocks
4. Headers and pins
5. Large capacitors
6. Any mechanical mounting components

**Best Practices:**
- Insert components from one side, solder from other
- Use proper support/fixture to keep board flat
- Trim leads after soldering
- Check for adequate solder flow through holes

**Purple Stepper Driver Installation:**
- Verify driver orientation (check pin 1 marking)
- Ensure all pins are straight before insertion
- Fully seat the driver (no gaps)
- Solder with adequate heat (avoid cold joints)
- Check for solder bridges between pins

---

## Purple Stepper Driver Specific Notes

### Driver Identification
- **Color:** Purple PCB
- **Type:** [TO BE DOCUMENTED]
- **Manufacturer:** [TO BE DOCUMENTED]
- **Model:** [TO BE DOCUMENTED]

### Key Differences from Red Drivers
*To be documented after comparison:*
- [ ] Pin configuration differences
- [ ] Voltage rating differences
- [ ] Current capacity differences
- [ ] Physical dimensions
- [ ] Mounting requirements

### Installation Steps
1. Check driver orientation (refer to marking on PCB and driver)
2. Verify pin count and spacing
3. Insert carefully to avoid bent pins
4. Ensure driver is fully seated
5. Solder all pins with good thermal contact
6. Inspect for solder bridges
7. Clean flux residue if required

### Post-Installation Checks
- [ ] Visual inspection of all solder joints
- [ ] Continuity test on power pins
- [ ] No shorts between adjacent pins
- [ ] Driver is firmly mounted
- [ ] Heatsink attached if required

---

## Soldering Techniques

### For SMD Components
**Reflow Method (if using oven/hot plate):**
- Preheat board to ~150°C
- Ramp to peak temperature (check solder paste spec)
- Hold at peak for appropriate time
- Cool down gradually

**Hand Soldering Method:**
- Use fine tip soldering iron (chisel or pointed)
- Temperature: 300-350°C (depending on component)
- Apply iron and solder simultaneously
- Use flux for better flow
- Clean tip frequently

### For Through-Hole Components
- Temperature: 350-400°C
- Heat both pad and component lead
- Apply solder to joint (not iron)
- Form proper solder fillet
- Avoid excessive solder

---

## Quality Checks

### Visual Inspection Checklist
- [ ] All components present and in correct location
- [ ] Correct component orientation (check polarity)
- [ ] No solder bridges between pads/pins
- [ ] Adequate solder on all joints
- [ ] No cold solder joints (dull, grainy appearance)
- [ ] No lifted pads or traces
- [ ] No flux residue (if no-clean flux not used)
- [ ] All component values match BOM

### Electrical Testing
1. **Pre-Power Checks:**
   - [ ] No shorts between power and ground
   - [ ] Continuity on power rails
   - [ ] No unexpected connections

2. **Initial Power-On:**
   - [ ] Apply power with current limit
   - [ ] Monitor current draw
   - [ ] Check for hot components
   - [ ] Verify regulated voltages

3. **Functional Testing:**
   - [ ] Stepper driver enable/disable
   - [ ] Motor movement in both directions
   - [ ] Microstepping operation
   - [ ] Current regulation
   - [ ] No abnormal noise or vibration

---

## Rework and Repair

### Common Issues and Fixes

#### Issue: Solder Bridge
**Fix:**
- Apply flux to the bridge
- Heat with soldering iron
- Use solder wick to absorb excess
- Clean with isopropyl alcohol

#### Issue: Cold Solder Joint
**Fix:**
- Add flux
- Reheat joint properly
- Add small amount of fresh solder if needed
- Ensure proper wetting

#### Issue: Component Wrong Orientation
**Fix:**
- Heat all joints simultaneously if possible
- Carefully lift component with tweezers
- Clean pads
- Re-apply solder paste/flux
- Install component correctly
- Resolder

#### Issue: Damaged Pad
**Fix:**
- Clean area
- Apply solder mask if available
- Create new pad with copper tape if necessary
- Use wire jumper if needed
- Test continuity

---

## Safety Considerations

### Soldering Safety
- Work in well-ventilated area
- Use fume extractor if available
- Wear safety glasses
- Keep soldering iron in stand when not in use
- Disconnect power when not in use

### ESD (Electrostatic Discharge) Protection
- Use ESD-safe workstation
- Wear ESD wrist strap connected to ground
- Store sensitive components in ESD bags
- Avoid synthetic clothing
- Use ESD-safe tools

### Handling Purple Stepper Drivers
- These components may be ESD-sensitive
- Handle by edges only
- Don't touch pins/pads directly
- Keep in anti-static packaging until installation

---

## Tools and Materials Required

### Essential Tools
- Soldering iron with temperature control
- Solder (lead or lead-free, as appropriate)
- Flux (liquid or paste)
- Tweezers (ESD-safe)
- Solder wick/braid
- Multimeter
- Magnifying glass or microscope
- Hot air station (for SMD rework)

### Optional Tools
- Reflow oven or hot plate
- Solder paste and stencil
- PCB holder/fixture
- Inspection camera
- Oscilloscope (for advanced testing)

### Materials
- Isopropyl alcohol (for cleaning)
- Lint-free wipes
- Anti-static bags
- Thermal paste (if heatsinks required)
- Wire for jumpers (if needed)

---

## Documentation and Tracking

### Assembly Records
For each board assembled, record:
- Date of assembly
- Board serial number (if applicable)
- Batch/lot numbers of components used
- Any deviations from standard assembly
- Test results
- Issues encountered and resolutions

### Lessons Learned
*(To be updated as assembly experience grows)*

1. **Purple Driver Specific:**
   - [To be documented]

2. **SMD Assembly:**
   - [To be documented]

3. **Through-Hole Assembly:**
   - [To be documented]

4. **Testing and QA:**
   - [To be documented]

---

## Troubleshooting Guide

### Board Won't Power On
- Check power supply connection
- Verify no short between power and ground
- Check LDO solder joints
- Verify input voltage is correct
- Check for reversed polarity components

### Stepper Drivers Not Working
- Verify driver orientation
- Check power supply to driver
- Verify logic signal connections
- Test enable pin
- Check for solder bridges on pins
- Measure voltage on driver power pins

### Excessive Heat
- Check for short circuits
- Verify current settings
- Check thermal connection to PCB
- Verify adequate ventilation
- Check trace current capacity

### Intermittent Issues
- Check for cold solder joints
- Verify all connections
- Check for loose components
- Test under vibration (if applicable)
- Check connector integrity

---

## References

### Related Documents
- [KICAD_ISSUES.md](./KICAD_ISSUES.md) - Known issues and tracking
- [CHANGES_NEEDED.md](./CHANGES_NEEDED.md) - Required KiCad changes
- README.md - Project overview

### External Resources
- Purple Stepper Driver Datasheet: [TO BE ADDED]
- PCB Soldering Standards (IPC-A-610)
- Component Manufacturer Guidelines
- Motor Control Best Practices

---

## Revision History

| Version | Date       | Changes | Author |
|---------|------------|---------|--------|
| 1.0     | 2026-02-07 | Initial document creation | Copilot |

---

## Contact and Support

For questions or issues during assembly:
- Open an issue on GitHub repository
- Reference Issue #2 for purple driver assembly
- Include photos of any problems encountered
- Provide detailed description of symptoms

---

**Last Updated:** 2026-02-07

**Status:** Living document - will be updated as more assembly experience is gained
