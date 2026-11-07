# Testing checklist

The project files were packaged from a supplied Proteus project and screenshots. **These tests have not been executed or certified.**

| Test | Procedure | Expected requirement | Verified |
|---|---|---|---|
| Supply rails | Measure VCC / GND and relay drive | Voltages within component ratings | No |
| Password entry | Set A3 A2 A1 A0 to `1011`, then activate Enter | Correct-code state occurs | No |
| Wrong password | Try `0000`, `1111`, `1010`, and other combinations | No authorization | No |
| Exhaustive combinations | Test every one of the 16 four-bit combinations | Only the intended code authorizes | No |
| Reset | Activate Reset after any state | State returns to intended idle/locked behavior | No |
| Enable switch | Toggle Enable | Gates the intended functions consistently | No |
| Relay output | Observe coil voltage and lamp state | Switches only when intentionally authorized | No |
| Power cycling | Restart simulation with input switches left in place | Starts in a defined safe state | No |
| Contact handling | Test simulated repeated Enter transitions | No unintended multiple toggles | No |

## Suggested evidence for future commits

Record a truth table with each four-bit combination, the comparator result, latched state, relay state, and lamp state. Capture verified *locked*, *valid password*, *invalid password*, and *reset* screenshots.

## Security context

A four-bit code has 16 combinations and is not adequate security for a deployed lock. There is no demonstrated lockout, tamper detection, rate limiting, nonvolatile secret storage, or encrypted communication.
