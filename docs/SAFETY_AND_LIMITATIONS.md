# Safety and limitations

## Simulation status

The source `.pdsprj` and two screenshots are included as supplied. This package is **not a verification report**. A Proteus file that can be opened is not evidence that each logic path and output state behaves correctly.

## Electrical safety

- Check 74HC IC power rails against device datasheets; do not connect an unregulated 9 V supply directly to 5 V-only logic.
- Verify relay-coil supply voltage, transistor bias, current rating and coil suppression (flyback diode).
- A BC557 is a PNP transistor; its emitter, collector, base bias and coil placement must match a correct PNP driver configuration.
- Keep low-voltage logic isolated from any external high-voltage loads.
- The 12 V lamp is a demonstration load. Do not connect mains AC to an unverified circuit.

## Security warning

The value `1011` is explicitly documented and **must not be treated as a secret credential**. Even a secret four-bit code is trivially enumerable. The design is suitable for education and portfolio presentation only.

## Missing artifacts

A native Proteus `.dsn` or PCB layout was not separately supplied. The `.pdsprj` is the provided native project artifact. No firmware or microcontroller code is required to describe the visible discrete-logic design, and none has been fabricated for this repository.
