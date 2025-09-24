**How do the pairwise correlations during the spontaneous period change from session-to-session?**
- Use the metadata to pick a mouse with a few different imaging sessions with the same FOV
- For each session:
  - Measure pairwise correlations in the pre and post spontaneous epochs
  - Compute the difference between these correlations
- Compare the difference across sessions
- If multiple mice (or FOV in the same mouse) meet these criteria, repeat across additional mice to see it differences are consistent


**Which neuron pairs have the largest changes in correlations after BCI learning? Do they increase or decrease? 
Are they also correlated to the conditioned neuron? What does their activity look like during the BCI task?**
- For a session of your choice, compute the pairwise correlations in the pre and post spontaneous epochs
- Compute the difference between these correlations
- Identify the pair of ROIs that has the largest (positive or negative) change. (Or select a few pairs that have particularly high differences)
- Look at the pairwise correlations of these neurons to the conditioned neuron. How does it compare to other neuron's correlation to the CN?
- Repeat across other sessions. 

**Do correlated neurons tend to have stronger connections? Use the photostimulation periods to measure connection strength across neurons based on their response latency and relate to spontaneous activity correlations.**
- For a session of your choice, compute the strength of connections during photostim epochs
  - For each trial, compute the strength of response of all neurons to the stimulation
  - Compute the distance of the neuron's from the stimulated ROI. (Each trial has one stimulated ROI). Find the centroids of the ROI masks, and compute the Euclidean distance between ROIs.
  - (Remember, the laser impacts neurons within ~25 um, so only consider effects >30um from the stimulated ROI)
  - Average across all trials for each stimulated neuron.
- How does the strength of the photostim connection relate to the correlations during spontaneous activity?
- Do the photostim connections change between pre and post photostim epochs?

**Do non-conditioned neurons change their activity during the BCI task? Were these cells more highly connected to the conditioned neuron prior to BCI learning?**
- For a session of your choice, look at neural activity during the BCI task
  - Do non-CN neurons activity relate to the behavior variables?
  - e.g. plot event-centered averages (take the activity of a neuron from ~2 seconds before to ~2 seconds after an event (say, threshold-crossing). What does this look like for CN neurons? What does it look like for non-CN neurons
  - Are these responses different based on how correlated the neuron is with the CN neuron (measured during spontaneous epoch)
  - Are neurons that are correlated during spontaneous epoch also correlated during BCI task?

**Do the transgenic/viral strategies impact any of the results you see?**
For any of the above questions (or questions of your own), can you see differences between the different approaches for expressing GCaMP and ChRmine? Or are the results more pronounced? 
