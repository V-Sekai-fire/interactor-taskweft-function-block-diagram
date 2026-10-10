# interactor-taskweft-function-block-diagram

A Lean 4 compiler from IEC 61131-3 function block diagrams to guest programs for the engine's RISC-V sandbox.

## What it is for

A diagram arrives as PLCopen XML, as a text form, or as a guest program lifted back, and the three forms round-trip. The compiler checks a diagram, plans its steps, simulates its scan over a trace and emits the guest program, refusing a diagram it cannot lower with a named reason. Signature tables under `sigs/` say which host calls a diagram may use. RFD 2157 owns the design.

## Build and run

```sh
lake build
lake exe taskweft_fbd_compiler check <diagram>
```

`Main.lean` lists the compiler's modes.

## Licence

MIT. See [LICENSE](LICENSE).
