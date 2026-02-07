# Issue Template for Purple Driver Assembly

Use this template to document specific issues found during the assembly and testing of boards with purple stepper motor drivers.

---

## Issue #[NUMBER]: [Brief Title]

**Date Discovered:** YYYY-MM-DD  
**Discovered By:** [Name]  
**Board Serial/Batch:** [If applicable]  
**Severity:** 🔴 Critical / 🟡 Medium / 🟢 Low  
**Status:** 🔍 Investigating / 🔧 In Progress / ✅ Resolved / ⏸️ Deferred

---

### Description
[Detailed description of the issue]

### Location
- **Schematic:** [Reference designator, page, section]
- **PCB:** [Layer, coordinates, reference designator]
- **Component:** [Part number, manufacturer]

### Symptoms
- [Observable symptom 1]
- [Observable symptom 2]

### Impact
- **Functionality:** [What doesn't work]
- **Performance:** [How performance is affected]
- **Safety:** [Any safety concerns]
- **Manufacturing:** [Impact on assembly process]

### Root Cause Analysis
[Analysis of why the issue occurred]

### Reproduction Steps
1. [Step 1]
2. [Step 2]
3. [Step 3]

### Workaround
[Temporary solution if available]

### Proposed Solution
[Permanent fix to be implemented in KiCad]

### Required Changes
- [ ] Schematic change
- [ ] PCB layout change
- [ ] BOM update
- [ ] Documentation update
- [ ] Testing procedure update

### Verification Plan
[How to verify the fix works]

### Related Issues
- Related to Issue #[NUMBER]
- See also: [Document reference]

### Photos/Diagrams
[Attach photos or create diagrams showing the issue]

### Notes
[Any additional relevant information]

---

## Example Issue Entry

## Issue #1: Stepper Driver Footprint Mismatch

**Date Discovered:** 2026-02-07  
**Discovered By:** icarusMQ  
**Board Serial/Batch:** Assembly Batch 2 (Purple Drivers)  
**Severity:** 🔴 Critical  
**Status:** 🔍 Investigating

---

### Description
During assembly of the purple stepper motor drivers, it was discovered that the footprint dimensions may not perfectly match the component. This requires verification and potential redesign.

### Location
- **Schematic:** U1, U2 (Stepper Driver symbols on page 2)
- **PCB:** Top layer, drivers located at coordinates [TBD]
- **Component:** Purple Stepper Motor Driver [Model TBD]

### Symptoms
- Potential pin misalignment
- Difficulty seating component fully
- Uncertain if all pins make proper contact

### Impact
- **Functionality:** May cause intermittent connection issues
- **Performance:** Could affect motor control reliability
- **Safety:** Potential for poor electrical contact and heating
- **Manufacturing:** Increases assembly difficulty and reject rate

### Root Cause Analysis
The original footprint was designed for red stepper drivers. Purple drivers may have different:
- Pin pitch (spacing between pins)
- Overall package dimensions
- Pin thickness
- Body size

### Reproduction Steps
1. Attempt to insert purple driver into PCB footprint
2. Observe fit and alignment
3. Check if all pins align with pads
4. Verify component can be fully seated

### Workaround
- Carefully align pins manually
- Apply force carefully to ensure full seating
- Verify electrical continuity after soldering
- Consider hand-bending pins slightly if necessary (not recommended)

### Proposed Solution
1. Obtain accurate datasheet for purple driver
2. Verify exact pin pitch and package dimensions
3. Update footprint in KiCad library
4. Modify PCB layout to use correct footprint
5. Generate new Gerbers for next board revision

### Required Changes
- [x] Schematic change - Update symbol properties
- [x] PCB layout change - Update footprint
- [x] BOM update - Update part number
- [x] Documentation update - Note footprint change in revision notes
- [ ] Testing procedure update - Add dimensional verification

### Verification Plan
1. Print PCB footprint at 1:1 scale
2. Place actual purple driver on printout
3. Verify pin alignment
4. Measure critical dimensions with calipers
5. Compare with datasheet specifications
6. Order test PCB with new footprint
7. Verify fit with actual components

### Related Issues
- Related to Issue #2 (Purple Driver Assembly)
- See also: KICAD_ISSUES.md Section 1
- See also: CHANGES_NEEDED.md - PCB Layout Changes

### Photos/Diagrams
[To be added: Photos of driver fit issue]

### Notes
- Priority: High - affects all future boards
- Consider making footprint compatible with both red and purple drivers if pin configurations allow
- May require board revision before next production run

---

## Template Usage Instructions

1. Copy the template section above
2. Replace [PLACEHOLDERS] with actual information
3. Fill in all relevant sections
4. Add to KICAD_ISSUES.md or create separate issue file
5. Update status as issue progresses
6. Link to related issues and documents

## Status Indicators

- 🔴 Critical - Prevents functionality, safety risk, or blocks assembly
- 🟡 Medium - Reduced performance or increased difficulty
- 🟢 Low - Minor issue, cosmetic, or documentation only

- 🔍 Investigating - Root cause not yet determined
- 🔧 In Progress - Solution is being implemented
- ✅ Resolved - Issue is fixed and verified
- ⏸️ Deferred - Issue acknowledged but postponed to future revision

## Issue Numbering

Issues should be numbered sequentially starting from 1. If tracking in GitHub Issues, reference the GitHub issue number.

Example: "Issue #5 (GitHub #2)" for the 5th documented issue which is also GitHub Issue #2

---

**Last Updated:** 2026-02-07
