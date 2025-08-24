---
layout: default
title: Home
---

<div style="width:100%;max-width:1500px;margin:0 auto">
  <div style="display:flex;align-items:flex-start;gap:20px;flex-wrap:wrap">

    <!-- Left side: Bio text -->
    <div style="flex:2;min-width:300px">
      <h1>Bahetihazi Maidu</h1>
      <p>Welcome to my personal webpage!</p>
  
      <p>I am a PhD student at the Mechanical Engineering Department at the University of Washington under the supervision of <a href="https://www.engr.washington.edu/facresearch/newfaculty/2019/delAlamo">Dr. Juan Carlos del Alamo</a>. Prior to joining del Alamo lab at UW, I obtained my master's degree at the Mechanical and Aerospace Engineering Department at the University of California San Diego where I specialized in computational modeling and cardiovascular fluid dynamics.</p>
  
      <p>My PhD research centers on the development of biomedical image–based, physics-informed deep learning approaches for reconstructing flow fields and stratifying cardiovascular disease risk from incomplete medical imaging data, with a specific focus on stroke risk assessments in the left atrium and left ventricle.</p>
  
      <p>Outside of work, I like hiking, taking road trips, and enjoying nature with families and friends.</p>
    </div>
  
    <!-- Right side: Bio photo -->
    <div style="flex:1;min-width:200px;text-align:center">
      <img src="/assets/bio.jpg" alt="Bahetihazi Maidu" style="max-width:100%;border-radius:12px;box-shadow:0 2px 6px rgba(0,0,0,0.2)">
    </div>

  </div>
</div>

---

# Most Recent Research and Publication Snippet

Left ventricular color-Doppler ultrasound imaging measures 1D flow velocity towards and away from the transducer on a 2D plane, missing complete flow information and pattern. Intraventricular vector flow mapping (VFM) technique has gained traction in the past decade to reconstruct 2D flow maps using color-Doppler images by integrating mass conservation equation. However, traditional VFM techniques do not consider momentum balance (e.g., Navier-Stokes equations) and remain sensitive to imaging artifacts. In our most recent work, we developed AI-VFM leveraging recent advances in physics-informed deep learning to reconstruct super-resolved and complete vector flow and pressure maps.

<!-- Page-specific CSS -->
<style>
.video-row {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  justify-content: flex-start;
}
.video-row video {
  width: 380px;          
  max-width: 100%;
  border-radius: 6px;    
  box-shadow: 0 2px 6px rgba(0,0,0,0.15); 
}
.video-container {
  position: relative;
  width: 380px; 
}

.video-title {
  text-align: center;
  font-weight: 600;
  margin-bottom: 5px;
}

.video-container video {
  width: 100%;
  border-radius: 6px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.15);
}

/* Overlay figure container */
.overlay-figure {
  position: absolute;
  top: 30px;
  right: 10px;
  text-align: center;
}

/* Overlay image */
.overlay-figure img {
  width: 40px;  
  border-radius: 0;
  display: block;
}

/* Overlay caption */
.overlay-caption {
  margin-top: 2px;
  font-size: 12px;
  color: white;
  text-shadow: 0 0 3px rgba(0,0,0,0.7);
}
</style>

<div class="video-row">
  <div class="video-container">
    <div class="video-title">Color-Doppler Images Radial Velocity</div>
    <video controls>
      <source src="/assets/VR_train.mp4" type="video/mp4">
    </video>
    <div class="overlay-figure">
      <img src="/assets/Dop_cbar.png" alt="Overlay figure">
      <div class="overlay-caption">m/s</div>
    </div>
  </div>

  <div class="video-container">
    <div class="video-title">Vector Velocity Field Reconstruction</div>
    <video controls>
      <source src="/assets/Vmag_pred.mp4" type="video/mp4">
    </video>
    <div class="overlay-figure">
      <img src="/assets/Vmag_cbar.png" alt="Overlay figure">
      <div class="overlay-caption">m/s</div>
    </div>
  </div>

  <div class="video-container">
    <div class="video-title">Pressure Field Reconstruction</div>
    <video controls>
      <source src="/assets/Pressure_pred.mp4" type="video/mp4">
    </video>
    <div class="overlay-figure">
      <img src="/assets/P_cbar.png" alt="Overlay figure">
      <div class="overlay-caption">mmHg</div>
    </div>
  </div>
</div>
