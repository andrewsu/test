# test

```
<script type='application/ld+json'>{
  "@context": "https://schema.org/", 
  "@id": "https://doi.org/10.5281/zenodo.1477956", 
  "@type": "Dataset", 
  "creator": [
    {
      "@type": "Person", 
      "affiliation": "Division of Medical Image Computing, German Cancer Research Center", 
      "name": "Wasserthal Jakob"
    }, 
    {
      "@type": "Person", 
      "affiliation": "Division of Medical Image Computing, German Cancer Research Center", 
      "name": "Neher Peter"
    }, 
    {
      "@type": "Person", 
      "affiliation": "Division of Medical Image Computing, German Cancer Research Center", 
      "name": "Maier-Hein Klaus"
    }
  ], 
  "datePublished": "2018-11-05", 
  "description": "<p>This dataset contains segmentations of 72 white matter tracts obtained from 105 subjects included in the Human Connectome Project (HCP) young adult dataset (https://www.humanconnectome.org/study/hcp-young-adult). The folder names correspond to the ID of the HCP subjects.</p>\n\n<p>The data is part of the following publication:&nbsp;&nbsp;<a href=\"https://doi.org/10.1016/j.neuroimage.2018.07.070\">Wasserthal et al., TractSeg - Fast and accurate white matter bundle segmentation. NeuroImage (2018)</a>. If you use the data please cite the paper.</p>\n\n<p>The tracts were extracted semi-automatically from whole-brain tractograms. For a detailed description of the tract segmentation process please refer to the paper. The following MRtrix (http://www.mrtrix.org/) commands were used to obtain the whole-brain tractograms:</p>\n\n<p>5ttgen fsl T1w_acpc_dc_restore_brain.nii.gz 5TT.mif -premasked<br>\ndwi2response msmt_5tt Diffusion.nii.gz 5TT.mif RF_WM.txt RF_GM.txt RF_CSF.txt -voxels RF_voxels.mif -fslgrad Diffusion.bvecs Diffusion.bvals<br>\ndwi2fod msmt_csd Diffusion.nii.gz RF_WM.txt WM_FODs.mif RF_GM.txt GM.mif RF_CSF.txt CSF.mif -mask nodif_brain_mask.nii.gz -fslgrad Diffusion.bvecs Diffusion.bvals<br>\ntckgen -algorithm iFOD2 WM_FODs.mif output.tck -act 5TT.mif -backtrack -crop_at_gmwmi -seed_image nodif_brain_mask.nii.gz -maxlength 250 -minlength 40 -number 10M -cutoff 0.06 -maxnum 0</p>\n\n<p>For &quot;CA&quot;, &quot;IFO_left&quot;, &quot;IFO_right&quot;, &quot;UF_left&quot;, &quot;UF_right&quot; we used tracking without anatomical constraints:</p>\n\n<p>tckgen -algorithm iFOD2 WM_FODs.mif output.tck -seed_image nodif_brain_mask.nii.gz -maxlength 250 -minlength 40 -number 10M -cutoff 0.06 -maxnum 0</p>\n\n<p>Due to their enormous size, the whole brain tractograms corresponding to the segmented tracts are not included this dataset. Please contact the author of the paper if you are interested in these tractograms.</p>\n\n<p>The following white matter tracts are included:</p>\n\n<p>1: AF_left &nbsp; &nbsp; &nbsp; &nbsp; (Arcuate fascicle)<br>\n2: AF_right<br>\n3: ATR_left &nbsp; &nbsp; &nbsp; &nbsp;(Anterior Thalamic Radiation)<br>\n4: ATR_right<br>\n5: CA &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Commissure Anterior)<br>\n6: CC_1 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Rostrum)<br>\n7: CC_2 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Genu)<br>\n8: CC_3 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Rostral body (Premotor))<br>\n9: CC_4 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Anterior midbody (Primary Motor))<br>\n10: CC_5 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; (Posterior midbody (Primary Somatosensory))<br>\n11: CC_6 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; (Isthmus)<br>\n12: CC_7 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; (Splenium)<br>\n13: CG_left &nbsp; &nbsp; &nbsp; &nbsp;(Cingulum left)<br>\n14: CG_right &nbsp;&nbsp;<br>\n15: CST_left &nbsp; &nbsp; &nbsp; (Corticospinal tract<br>\n16: CST_right&nbsp;<br>\n17: MLF_left &nbsp; &nbsp; &nbsp; (Middle longitudinal fascicle)<br>\n18: MLF_right<br>\n19: FPT_left &nbsp; &nbsp; &nbsp; (Fronto-pontine tract)<br>\n20: FPT_right&nbsp;<br>\n21: FX_left &nbsp; &nbsp; &nbsp; &nbsp;(Fornix)<br>\n22: FX_right<br>\n23: ICP_left &nbsp; &nbsp; &nbsp; (Inferior cerebellar peduncle)<br>\n24: ICP_right&nbsp;<br>\n25: IFO_left &nbsp; &nbsp; &nbsp; (Inferior occipito-frontal fascicle)&nbsp;<br>\n26: IFO_right<br>\n27: ILF_left &nbsp; &nbsp; &nbsp; (Inferior longitudinal fascicle)&nbsp;<br>\n28: ILF_right&nbsp;<br>\n29: MCP &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;(Middle cerebellar peduncle)<br>\n30: OR_left &nbsp; &nbsp; &nbsp; &nbsp;(Optic radiation)&nbsp;<br>\n31: OR_right<br>\n32: POPT_left &nbsp; &nbsp; &nbsp;(Parieto\u2010occipital pontine)<br>\n33: POPT_right&nbsp;<br>\n34: SCP_left &nbsp; &nbsp; &nbsp; (Superior cerebellar peduncle)<br>\n35: SCP_right&nbsp;<br>\n36: SLF_I_left &nbsp; &nbsp; (Superior longitudinal fascicle I)<br>\n37: SLF_I_right&nbsp;<br>\n38: SLF_II_left &nbsp; &nbsp;(Superior longitudinal fascicle II)<br>\n39: SLF_II_right<br>\n40: SLF_III_left &nbsp; (Superior longitudinal fascicle III)<br>\n41: SLF_III_right&nbsp;<br>\n42: STR_left &nbsp; &nbsp; &nbsp; (Superior Thalamic Radiation)<br>\n43: STR_right&nbsp;<br>\n44: UF_left &nbsp; &nbsp; &nbsp; &nbsp;(Uncinate fascicle)&nbsp;<br>\n45: UF_right&nbsp;<br>\n46: CC &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; (Corpus Callosum - all)<br>\n47: T_PREF_left &nbsp; &nbsp;(Thalamo-prefrontal)<br>\n48: T_PREF_right&nbsp;<br>\n49: T_PREM_left &nbsp; &nbsp;(Thalamo-premotor)<br>\n50: T_PREM_right&nbsp;<br>\n51: T_PREC_left &nbsp; &nbsp;(Thalamo-precentral)<br>\n52: T_PREC_right&nbsp;<br>\n53: T_POSTC_left &nbsp; (Thalamo-postcentral)<br>\n54: T_POSTC_right&nbsp;<br>\n55: T_PAR_left &nbsp; &nbsp; (Thalamo-parietal)<br>\n56: T_PAR_right&nbsp;<br>\n57: T_OCC_left &nbsp; &nbsp; (Thalamo-occipital)<br>\n58: T_OCC_right&nbsp;<br>\n59: ST_FO_left &nbsp; &nbsp; (Striato-fronto-orbital)<br>\n60: ST_FO_right&nbsp;<br>\n61: ST_PREF_left &nbsp; (Striato-prefrontal)<br>\n62: ST_PREF_right&nbsp;<br>\n63: ST_PREM_left &nbsp; (Striato-premotor)<br>\n64: ST_PREM_right&nbsp;<br>\n65: ST_PREC_left &nbsp; (Striato-precentral)<br>\n66: ST_PREC_right&nbsp;<br>\n67: ST_POSTC_left &nbsp;(Striato-postcentral)<br>\n68: ST_POSTC_right<br>\n69: ST_PAR_left &nbsp; &nbsp;(Striato-parietal)<br>\n70: ST_PAR_right&nbsp;<br>\n71: ST_OCC_left &nbsp; &nbsp;(Striato-occipital)<br>\n72: ST_OCC_right<br>\n&nbsp;</p>\n\n<p>From version 1.2.0 of this dataset onwards it uses the newest trackvis (trk) standard (using nibabel.streamlines API). Streamlines are saved in native voxel space and when loaded are transformed to coordinate space using the affine stored in the trk file header. In the previous versions of the dataset the older nibabel.trackvis API was used (streamlines are saved in real coordinate space and no affine is applied when loading them).</p>", 
  "distribution": [
    {
      "@type": "DataDownload", 
      "contentUrl": "https://zenodo.org/api/files/bd24dafb-672e-45f5-adb2-4713af82909b/HCP105_Zenodo_NewTrkFormat.zip", 
      "fileFormat": "zip"
    }
  ], 
  "identifier": "https://doi.org/10.5281/zenodo.1477956", 
  "keywords": [
    "dMRI, Tractography, White Matter, Human Connectome Project, Diffusion MRI, Connectomics, Segmentation"
  ], 
  "license": "https://creativecommons.org/licenses/by-nc/4.0/", 
  "name": "High quality white matter reference tracts", 
  "url": "https://zenodo.org/record/1477956", 
  "version": "1.2.0"
}</script>
```
