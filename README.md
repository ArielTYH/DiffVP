# DiffVP
DiffVP: Differential Visual Semantic Prompting for LLM-Based CT Report Generation

All codes will be realesed.

The overview of our work :
<img width="4518" height="1779" alt="overview" src="https://github.com/user-attachments/assets/c6e738bf-2918-4688-a97b-cab8fa7f0eb1" />
The framework takes a target CT volume and a normal reference CT as inputs. A shared visual encoder and resampler produce aligned latent tokens ($I$ and $I^{r}$). A difference-aware module then derives:  
(a) a global delta $\Delta_{\text{global}}$ by applying a Transformer with a learnable query over $I$ and $I^{r}$; and  
(b) a local delta $\Delta_{\text{local}}$ by aggregating token-wise residuals with distance-based importance weights.  

These two signals are then fused by  
(c) a difference-to-prompt generator, which forms a visual difference prompt. This prompt is prepended as a soft prefix to a LoRA-tuned LLM to guide medical report generation.

