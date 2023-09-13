# notion
Here I save a bunch of useful html code snippets for personalized notion widgets
```rust
/*
  This test injects a fault in the threshold of the third neuron of the second layer.
  - neuron corresponding to the digit 2
  - bit at index 62 from 0 to 1
  - threshold from 1.0 to infinity

  Increasing the threshold above infinity we expect the neuron to **never fire**
  - the digit 2 will never be recognized
  - resulting accuracy = 89.0%
*/

// MANUAL FAULT INJECTION
//***************************************************************************
let fault_type: FaultType = FaultType::StuckAt1;
let time_step: Option<u64> = None;
let layer_index: usize = 1;
let component_category: ComponentCategory = ComponentCategory::MemoryArea;
let component_type: ComponentType = ComponentType::Threshold;
let component_index: usize = 2;
let bit_index: Option<usize> = Some(62);
//***************************************************************************
```
