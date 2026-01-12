
# PROVEN
PROVEN
=======
# A Two-Stage Visual Memory Retention Network for CBCT-guided Transbronchial Peripheral Lung Lesion Biopsy Navigation
We introduce PROVEN, a two-stage Visual Memory Retention Network designed for CBCT-guided transbronchial peripheral lung lesion biopsy navigation. The framework follows a stage-wise learning strategy, comprising a domain knowledge preparation stage and a domain knowledge learning stage. In the first stage, contrastive pretraining is used to encode domain-specific representations, enabling coarse anatomical alignment and reducing the deformation search space. In the second stage, a plug-and-play Visual Memory Retention (VMR) module is incorporated to capture cross-phase spatiotemporal dependencies, thereby enhancing feature consistency and stabilizing anatomical alignment under CT–body divergence (CTBD). To further leverage temporal redundancy, a Multi-dimensional Representation Mixer (MDRM) is employed to model temporal continuity, preserve motion plausibility, and improve registration robustness in CTBD-affected regions. Experimental evaluations demonstrate that PROVEN consistently outperforms existing deformable registration methods, highlighting its potential for clinical applications such as electromagnetic navigation bronchoscopy.
In addition, we establish a standardized paired preoperative CT–intraoperative CBCT lung dataset to support future research on intraoperative navigation for lung cancer. The dataset is being anonymized and reorganized to ensure privacy protection and ease of access. Currently, seven paired CT–CBCT cases have been released for evaluation, with further data to be made available.
# Dataset
## Inclusion Criteria
The in-house clinical dataset was curated according to the following criteria: patients had multiple phase-resolved lung CBCT scans acquired during treatment; lesions exceeded 5 mm in size; both preoperative planning CT and admission CT images were available; and cases with severe motion artifacts were excluded.
## Data Modality
The in-house clinical dataset comprises temporally paired CT and CBCT scans, including preoperative planning CT images and respiratory-gated multi-phase CBCT volumes acquired during surgery.
## Landmark Annotation
Landmarks were selected at salient vascular and tracheal bifurcation points and other prominent anatomical structures identifiable across imaging time points for the same patient. To ensure annotation reliability, an inter-rater agreement analysis was performed by computing the Kappa coefficient among multiple annotators. Annotations with Kappa values below 0.6 were further reviewed and refined, whereas values of 0.6 or higher were considered to indicate acceptable agreement for subsequent analysis.
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/keypointRevise.png?raw=true" width="900" alt="demo"/><br/>

## Dynamic Respiratory Motion Registration Results
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/yiying1.png?raw=true" width="1200" alt="demo"/><br/>

<table>
<tr>
<td align="center">
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/2drendering.gif?raw=true" width="300"/><br/>
2D rendering of respiratory motion after registration
</td>

<td align="center">
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/3drendering.gif?raw=true" width="300"/><br/>
3D rendering of respiratory motion after registration
</td>

<td align="center">
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/tumorrendering.gif?raw=true" width="300"/><br/>
Spatiotemporal tumor variation across phases after registration
</td>
</tr>
</table>


<div style="display: flex; justify-content: space-between;"> 
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/without_MDRM.gif?raw=true" width="300" alt="demo"/> 
<img src="https://github.com/computerAItest/PROVEN/blob/main/PROVEN/data/with_MDRM.gif?raw=true" width="300" alt="demo"/> 

</div> 
Without MDRM: discontinuous and jittery motion &nbsp;&nbsp; With MDRM: smooth and continuous motion


