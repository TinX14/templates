HCP-MMP parcellation in volume space

Reference: Glasser et al., 2016, Nature. 
Surface Atlas: Glasser_et_al_2016_HCP_MMP1.0_StudyData: https://balsa.wustl.edu/sceneFile/show/L731

Note: This volume atlas (converted from surface) is not recommended, although I did convertion here. Keep in mind that the surface-to-volume is not accurate... It's better to reconstruct individual surface and register to 32k_fs_LR template surface then apply the surface atlas. 

How was this volume atlas done?
1) label to volume mapping from surface to volume (from the midthickness surface to map labels to voxels in 8mm)

Glasser_et_al_2016:/HCP_PhaseTwo/Q1-Q6_RelatedParcellation210/MNINonLinear/fsaverage_LR32k/Q1-Q6_RelatedParcellation210.?.CorticalAreas_dil_Colors.32k_fs_LR.dlabel.nii to Glasser_et_al_2016:/HCP_PhaseTwo/Q1-Q6_RelatedParcellation210/MNINonLinear/Q1-Q6_RelatedParcellation210_AverageT1w_restore.nii.gz

2) apply volume brain mask, gray probability mask (>0.75) 

$FSLDIR/data/standard/MNI152_T1_1mm_brain_mask.nii.gz
$FSLDIR/data/atlases/MNI/MNI-maxprob-thr25-1mm.nii.gz


3) Color tables were exported from the original label files


