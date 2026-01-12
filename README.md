
# PROVEN
PROVEN
=======
# A Two-Stage Visual Memory Retention Network for CBCT-guided Transbronchial Peripheral Lung Lesion Biopsy Navigation
We propose PROVEN, a novel two-stage Visual Memory Retention Network for CBCT-guided transbronchial peripheral lung lesion biopsy navigation. Inspired by the human stage-wise learning paradigm, PROVEN consists of two sequential stages: a domain knowledge preparation stage and a domain knowledge learning stage. In the domain knowledge preparation stage, contrastive learning–based pretraining is employed to accumulate domain-specific knowledge, guiding coarse alignment of paired topological structures while effectively reducing the search space. Subsequently, a plug-and-play Visual Memory Retention (VMR) module is introduced to model spatiotemporal relationships across different phases, reinforcing feature consistency and ensuring stable anatomical alignment under CT–body divergence (CTBD)-induced deformations for more precise structural matching. In addition, to exploit inter-frame redundancy, we develop a Multi-dimensional Representation Mixer (MDRM) to model temporal continuity, preserve the physical plausibility of motion, and enhance registration robustness in CTBD-affected regions. Extensive qualitative and quantitative results demonstrate that PROVEN outperforms existing deformable registration methods, providing strong support for clinical applications such as electromagnetic navigation bronchoscopy.
In this study, we construct a standardized paired preoperative CT–intraoperative CBCT lung dataset to facilitate future research on intraoperative navigation for lung cancer. The data are currently being anonymized to remove all private information and further organized and converted to ensure faster and more convenient access. At present, seven paired datasets for preoperative CT and intraoperative CBCT registration-based navigation have been released for evaluation, with additional data to be uploaded soon.
# Dataset
## Inclusion Criteria
The in-house clinical dataset includes several inclusion criteria: (a) each patient underwent multiple sets of lung CBCT images at different phases during treatment; (b) the lesion volume must be greater than 5mm; (c) preoperative planning CT and admission CT imaging results were recorded; (d) images with significant motion artifacts were excluded.
## Data Modality
The in-house clinical dataset consists of paired CT–CBCT imaging scans acquired from patients at different time points, including preoperative planning CT scans and multi-phase CBCT data obtained intraoperatively using respiratory gating.
## Landmark Annotation
The landmarks we used are primarily based on key vascular or tracheal junctions and prominent anatomical features, which are identified from imaging the same patient at different time points. These landmarks demonstrate high consistency across different evaluators.
We conducted an inter-rater consistency analysis to validate the reliability of the manual contour/landmark annotations. Specifically, we calculated the Kappa coefficient by comparing the annotations made by multiple evaluators to assess the level of agreement. If the Kappa value is below 0.6, we will further review and refine the annotations. If the Kappa value is 0.6 or above, it indicates significant consistency, and the annotations are considered reliable for subsequent analysis.
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
2Without MDRM: discontinuous and jittery motion &nbsp;&nbsp; With MDRM: smooth and continuous motion


