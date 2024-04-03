# POSER
Marine Photogrammetry Simulator - Blender 3D


Summary

Photogrammetry has become a common mechanism for the documentation of underwater structures. Numerous academic and government agencies routinely publish results inferring from photogrammetric models, using varying, and often non-standardized, acquisition methodologies. In many cases the complexities and challenges intrinsic to oceanographic field captured data have left us little choice but to accept results without appropriate validation. Working in a cross-discipline team of oceanographers, archaeologists, metrology experts, data analysts, and instructional designers, we have devised a highly versatile empirical framework to test and compare the common methods used in large scale underwater structure from motion (SFM) and multi-view stereo (MVS) reconstruction, to help establish and communicate best practices, and to educate the community regarding the key principles at play and clearly demonstrate the effects of improper data acquisition strategies. We employ a customizable open source digital simulator, made publicly available, with the goal of beginning the communal, cross disciplinary development of rigorous standards for field captured data.

A short video describing the system is available here, showing a preliminary version made to test camera acquisition pathways and conditions: https://youtu.be/zQ4lXENWbes

Full project outline

In recent years, the potentialities of simulation platforms have become increasingly evident both for research purposes (Nakath et al., 2022; Wang et al, 2019) and educational goals (Luhmann et al., 2022). Among the different reasons, we can include: the possibility to simulate environments that are difficult to access, perform a statistically significant number of tests, lowering costs, the possibility of systematically varying and controlling the different variables involved. Still, simulation solutions present limitations, as evidenced by the fact that it remains a very active research topic. At the same time, the potential offered by these solutions is undeniable in the educational context or in cases where researchers and practitioners have limited resources.

The aim of this project is to build an educational simulation platform, as a means to create a Learning environment where idealized scenarios and datasets for underwater photogrammetry will enable students and practitioners to actively learn surveying skills and best practices by isolating relevant variables within a closed environment. So, while the project primarily pursues educational purposes, it will certainly also contribute to the improvement of simulation platforms in a research context.

Our framework will be released as open source to allow for easy adaptation to different educational and training needs. Students and practitioners will have the opportunity to learn about basic concepts of survey planning, camera calibration, interior and exterior orientation in underwater photogrammetry.

The simulator (Giuseffi 2020) is implemented to show, in real time, the movement of the camera over a scene, with an adjacent view of the camera’s local view (fig. 1). The results of these simulations output experimental image sets which can then be processed in different photogrammetric software solutions and analyzed to show differences in the achievable potential accuracy. For example, a preliminary comparison of common acquisition pathways used by NOAA, National Parks Service, and Scripps Institution of Oceanography researchers is depicted in fig.2.

Figure 1: side by side view, 3d scene and moving camera input Figure 2: Agisoft point confidence values, processing images of the same synthetic environment with varying acquisition patterns (lawnmower, spiral, double-grid)

CHARACTERISTICS OF POSER

POSER is currently built on the open source Blender 3D graphics platform, which offers a powerful extensible rendering engine with a python backend, enabling scripted batch processing and easily reproducible pipelines.

POSER will incorporate metrologically sound 3D datasets, including sub millimeter 3d scans of coral and artifacts, along with simple primitive shapes and varying topographies. These datasets will be sourced, in part, from the 2023 ISPRS Nautilus project and, at the same time, datasets created with POSER will contribute to the NAUTILUS web portal. Datasets will be annotated separately, to enable comparison of key metrics related to their representations resulting from virtual photogrammetry simulation. POSER’s team will work towards the possibility for trainers to be able to integrate their own datasets to cover the specific teaching aspects they want to cover in their classes.

Objects will feature optional custom materials which are optimized for photogrammetric experimentation, including scalable random voronoi patterns and other fractal patterns. A rigorous yet flexible modelling of water air glass interfaces (Nakath et al., 2022) for underwater dome vs flat ports analyses and comparisons will be implemented.

In POSER, users will be able to experiment not only with different photogrammetric acquisition strategies, but also to test the influence on the final accuracy of the distribution of control and scaling elements, such as scale bars and markers. Moreover, different camera configurations will be implementable: from single, to stereo and multi-camera rigs.

POSER will enable the computation of simple, yet effective path planning information, such as, for example, estimated number of photographs and estimated completion time. Moreover, the time stamped computed trajectory will provide key data for practitioners to understand the feasibility of a planned dive with respect to autonomy of the battery of a remotely operated or unmanned vehicle or, most importantly, safety of a SCUBA operated dive (Aristidou and Michael, 2014; Mangeruga et al., 2020). Indeed, according to average swimming speed (or diver propulsion vehicle) non decompression limits, non decompression sickness triggering events, air consumption can be computed through an ad hoc export of the depth vs time data and its analysis in open source packages like Subsurface divelog (https://subsurface-divelog.org).

EDUCATIONAL AND DISSEMINATION ACTIVITIES

A substantial amount of project activities will concern the creation of teaching and dissemination materials, such as video tutorials with example case studies, online wikis, to facilitate and support the use of the POSER by both instructors and learners.

At the end of the project, an online workshop with an associated data challenge will be organised to promote the dissemination and use of POSER within the extended community.

REFERENCES

Aristidou, K. and Michael, D., 2014. Towards building a diving simulator for organizing dives in real conditions. WSCG2014 Conference on Computer Graphics, Visualization and Computer Vision.

Giuseffi, L. (2020). Using Technology to Improve Conservation: Virtual Environments for Testing Actionable Metrics of Scientific Methodology for Measuring Coral Recruits in the Field. UC San Diego: Center for Marine Biodiversity and Conservation. Retrieved from https://escholarship.org/uc/item/6hp3946d

Luhmann, T., Chizhova, M., Gorkovchuk, D., Popovas, D., Gorkovchuk, J. and Hess, M., 2022. Development of terrestrial laser scanning simulator. The International Archives of the Photogrammetry, Remote Sensing and Spatial Information Sciences, 46, pp.329-334.

Mangeruga, M., Casavola, A., Pupo, F. and Bruno, F., 2020. An underwater pathfinding algorithm for optimised planning of survey dives. Remote Sensing, 12(23), p.3974. Nakath, D., She, M., Song, Y. and Köser, K., 2022. An Optical Digital Twin for Underwater Photogrammetry: GEODT—A Geometrically Verified Optical Digital Twin for Development, Evaluation, Training, Testing and Tuning of Multi-Media Refractive Algorithms. PFG–Journal of Photogrammetry, Remote Sensing and Geoinformation Science, 90(1), pp.69-81. Wang, J., Zhou, Y., Li, B., Meng, Q., Rocco, E. and Saiani, A., 2019. Can underwater environment simulation

contribute to vision tasks for autonomous systems? Presented at the 2nd UK Robotics and Autonomous Systems Conference, (UK-RAS 2019), Loughborough University, 24th January.

Expected outcomes

- An open source, reconfigurable photogrammetry simulator incorporating sound metrology with real world assets of known dimensions.

- An integrated framework to evaluate photogrammetry data, quantifying overlap, resolution, angular coverage, individual image quality, and deviation from baseline.

- An integrated framework to replicate water refractive effects into a virtual environment

- An integrated framework to simulate light dropoff and surface caustics

- An integrated framework for SCUBA dive planning to enhance non decompression limits and air consumption awareness (using for example the open source project Subsurface)

- A project repository hosting the system and related datasets.

- Develop a curriculum with educational materials and documentation showing users how to employ the animated system, stage experiments, and extract metrics.

- A community workshop to introduce the system.

- A journal article detailing the replicable results of several experiments, including:

o acquisition path comparisons (aerial-like with and without cross strips, vs. spiral, )

o nadir and oblique imaging

o different turbidity

o flat and uncentered dome ports

o multicam platform comparison, including synced vs unsynced camera setups
