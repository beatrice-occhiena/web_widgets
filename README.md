# notion
Here I save a bunch of useful html code snippets for personalized notion widgets
```rust
pub struct SNN < N: Neuron + Clone + Send + 'static >
{
  layers:  Vec<Arc<Mutex<Layer<N>>>>,
}

pub fn process_input(
  &mut self,
  input_rc: Receiver<SpikeEvent>, output_tx: Sender<SpikeEvent>,
  fault: Option<InjectedFault>)
{
```
