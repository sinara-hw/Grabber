# CHANGELOG

All notable changes to Grabber-DIOT are documented in this file.

## v2.0

**Release owner:** Mikołaj Sowiński (TS)

**Designers:** 
- Krzysztof Belewicz (WUT)

**Reviewers:** 
- Maciej Przybysz (TS)
- Marta Fąfara (TS)

**Contributors:** 
- Marcin Kiepiela (TS)

**Funded by:** 
- WUT ISE
- Technosystem

All schematic files updated according to DIOT template v1.4.  
Changes in respect to the previous revision:

added project parameters:
- link to repository  
- version number, moved to 2.0
- authors, contributors, reviewers 

Grabber_DIOT.SchDoc:
- added note about EEM/DIOT pair count mismatch (#12)
- merged old pages "Grabber_DIOT_TOP.SchDoc" and "Grabber_DIOT.SchDoc"
- moved EEPROMs, fiducials, mounting holes, ESD strips, front panel connectors, power LEDs/testpoints to their dedicated pages
- LVDS_repeater sheet symbol blocks renamed to U_LVDS_repeaterN
- misaligned U_LVDS_repeater block shifted

LVDS_repeater.SchDoc:
- C47 changed from 0402 100nF 16V to 0402 100nF 50V to reduce BOM count
- improved readability
- pin swapped TVS diode for easier routing
- TVS diode changed from NUP4114UPXV6T1G to D1213A-04V-7

Power_Supplies.SchDoc
- added power budget
- 3V3 DCDC regulator divider corrected from 3.43V to 3.3V
- C67/C65/C59 changed from 0402 100nF 16V to 0402 100nF 50V to reduce BOM count

FP_Connectors.SchDoc
- J1/J2 moved here from Top level page in previous revision
- aligned net labels and improved readability

EEM_Connectors.SchDoc
- added note about EEM/DIOT pair count mismatch (#12)

Temperature_monitoring.SchDoc
- corrected pull-up note on  to point to Power_Supplies.SchDoc

PCB changes:
- fixed board outline, front panel connectors positioned according to lower-left FP mounting hole in previous revision
- added case mounting holes/ ESD strips/ keepout regions from DIOT template
- added front panel/case 3d models from DIOT template
- layers renamed to match DIOT template
- vias changed to 0.25/0.5 to match aisler base requirements
- rules modified to match aisler base requirements (min. trace/separation)
- drc masking fixed to actually check said rules
- Updated stackup to the unified 4 layer 1.6mm version
- length matched DIOT/EEM signals
- corrected impedance geometry table values
- rearranged LVDS drivers for better routing, fixed shared GND vias
- fixed GND plane discontinuity below LVDS pairs (P3V3 plane below LVDS drivers, P12V0 plane below BP signals)
- majority of LVDS pairs moved to bottom layer to reduce stubs to connector pins and TVS diodes at LVDS drivers
- reduced amount of layer changes for LVDS pairs between EEM-DIOT connectors
- fixed xSignal CL_LVDS incorrectly routing through TVS diode at LVDS drivers (nets YCLK, ZCLK, Z3)
- synchronized rooms/footprint names with schematic
- cleared lingering DRC violations
- corrected Unrouted Net rule
- changed bottom layer allowed height to 1.6mm
- removed unused rules from the project
- L2/P3V3 connection marked in rules and corrected
- adjusted copper balancing dimensions/ clearances
- improved P12V0 polygon on top layer
- differential traces CC3, CC1, XCLK, X1 - added more GND vias near layer change
- copper balancing keepout pattern left outside of the board
- front panel LEDs changed to Dialight 571-0112F, adjusted connector positions
- added note about ZCLK/ Z0-Z3 on the silkscreen layer



---

## Prior releases

**Designers:**
- Grzegorz Kasprowicz (WUT)
- Mariusz Mróz (WUT)
- Maciej Przybysz (TS)

**Reviewers:**
- unspecified

**Contributors:**
- unspecified