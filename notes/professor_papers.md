# PhD Research Notes 
— Professor Papers *Lencho Ajema Negese | github.com/lenchoajema | ORCID: 0009-0004-6093-8890* *Updated: June 25, 2026* 
## Prof. Jordan Aaron 
Engineering Geology, ETH Zurich **Google Scholar:** scholar.google.com/citations?user=v4JjOwQAAAAJ **Research focus:** Debris flow dynamics, LiDAR sensing, CV for geohazards 
### Paper 1: High-Frequency 3D LiDAR Measurements of a Debris Flow (GRL, 2023) 
- **Key contribution:** First subsecond 3D point cloud measurements of full-scale debris flows at Illgraben, Valais. Derives front and surface velocity from successive scans.
- **3 things I learned:** - LiDAR-derived velocity fields are the 3D equivalent of what optical flow does in 2D video — motion estimation from dense sequential sensor data
-  The Illgraben site produces ~10 debris flows per year — enough for a meaningful ML training dataset
-   Internal flow dynamics (surges, levées) were previously invisible without subsecond resolution
-   **My connection:** My UAV thesis extracted motion features and classified events from aerial image time-series. The core problem is identical - derive dynamic measurements from dense sequential sensor data to classify physical events. 
- **Question for Prof. Aaron:** 
-      How do you handle the domain shift between the Illgraben dataset and other debris flow sites with different rheology and grain size distributions? 
### Paper 2: DeFlow — Self-supervised 3D Motion Estimation of Debris Flow (CVPRW 2023, Best Paper) 
- **Key contribution:** Self-supervised scene flow model combining LiDAR + camera. Multi-level sensor fusion. Temporal processing for flow speed estimation over time. 
- **3 things I learned:** - Self-supervision removes the need for expensive manual annotation — critical for geoscience datasets - Multi-level sensor fusion (2D camera + 3D LiDAR) outperforms either modality alone — directly motivates the Road Safety sensor fusion work - The temporal processing module is architecturally similar to the spatiotemporal feature extraction I used in my thesis
- **My connection:** My thesis used CNNs for spatiotemporal feature extraction across UAV image sequences. DeFlow does the same across LiDAR+camera sequences. The abstraction level is the same — I understand this architecture.
- **Open research direction I see:** DeFlow uses self-supervision with inductive biases from the physical scene. Incorporating physics-based priors (debris flow rheology, slope geometry) into the loss function could further constrain learning. 
### Paper 3: Deep Learning Object Detection on LiDAR-Derived Data for Debris Flow (NHESS, Dec 2025) 
- **Key contribution:** Converts high-res LiDAR point clouds into hillshade images → applies YOLOv8 / Faster-RCNN for debris flow component detection. 
**3 things I learned:** - The hillshade representation bridges the gap between 3D point clouds and standard 2D detection models — a practical engineering solution - Object detection identifies flow components (snout, body, levées) at high temporal resolution — enabling automated characterisation that was previously manual - This is the exact pipeline the PhD position is being hired to extend and improve
- **My connection:** I have direct experience with CNN-based detection pipelines (MSc thesis on UAV target detection). 
The hillshade-to-detection approach uses the same architectures I have studied and understand. 
## Prof. Bryan T. Adey 
- Infrastructure Management, ETH Zurich **Google Scholar:** scholar.google.com/citations?user=b2qBTKgAAAAJ **Research focus:** Infrastructure resilience, ML for asset management, transport networks
- ### Resilience Assessment Framework (FORESEE Project, 2024)
- **Key contribution:** Guidelines for estimating transport infrastructure resilience using data management plans designed to enable ML-based analysis. 
- **3 things I learned:**
- Resilience is defined across 4 phases: absorption, adaptation, restoration, preparedness
-   surrogate models must assess each phase
- Data standardisation is a prerequisite for ML resilience analysis - data engineering is as important as modelling
-  The framework was designed to scale from asset-level to network-level
-  surrogate models must operate across all three scales **Connection to SHIFTIN PhD:** The position I applied for is building the ML surrogate models this framework calls for. 
### UN Stress Test Framework for Inland Transport (ECE/TRANS/WP.5/GE.3/2023/3, Published 2024) 
**Key contribution:** UN-level methodology for stress testing transport infrastructure under climate hazards. 
**Key insight:** Adey operates at the policy level. Surrogate models must produce outputs that are interpretable by infrastructure managers and policymakers — not just accurate. Explainability is a requirement, not a nice-to-have. 
**Research direction I'm interested in:** Surrogate model architectures that produce uncertainty estimates alongside predictions 
— enabling risk-aware decision-making that infrastructure managers can trust. 
## Papers to read next (Week 2) 
- [ ] Prof. Adey — SHIFTIN project publications (when available on ETH research portal)
- [ ] DeFlow follow-up: arxiv.org/abs/2304.02569 full method section
- [ ] Optical flow for geoscience: MicroFlow paper (arxiv.org/pdf/2504.13452) 
- [ ] Prof. Alrabaee (UAEU) — network security + deep learning papers
