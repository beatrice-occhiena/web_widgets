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

  pub fn process_input(&self, spikes: &Vec<Vec<u8>>, injected_fault: Option<InjectedFault>) -> Vec<Vec<u8>> {

    // PRE-PROCESSING: convert the input spikes into spike events
    let input_spike_events = self.derive_input_spike_events(spikes);

    // PARALLEL PROCESSING: process the input spike events
    let output_spike_events = self.process_input_spike_events(input_spike_events, injected_fault);
    //let output_spike_events = self.verbose_process_input_spike_events(input_spike_events);

    // POST-PROCESSING: convert the output spike events into output spikes
    let output_spikes = self.derive_output_spikes(&output_spike_events, spikes.first().unwrap().len());

    output_spikes   
  }
```
