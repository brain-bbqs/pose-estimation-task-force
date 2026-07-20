# Pose Estimation Task Force

Placeholder repository for issues related to the pose estimation task force.



## Phase Plan

The mission of this project is quite extensive in scope.
As such, we are carefully planning each stage as limited, achievable steps, which will gradually accumulate the capabilities of the system.
We thus state the following milestones with expected deliverable dates and subtasks.

### All Phases

- Dataset-specific RAG-style methods will be assessed and used throughout each phase.
- Individual models will be trained per video and per dataset of consistent videos.
- Mixtures of experts will be made across datasets.
- Long-running cumulative models will be trained continuously over the entire collection.

### Phase 1a (December 2026)

i. Collect a centralized collection of videos with top-down or bottom-up fixed camera field of views of caged rodents.
ii. Transcode all videos in the collection to a common physical or coordinate space.
iii. Work with the scientific community to define rigorous, well-documented, and anatomically justified standard skeleton definitions (at both coarse- and fine- levels of detail).
iv. Release beta version of the web-based crowd-sourced labeler for training frames, which reads from the transcoded videos on EMBER and writes all annotations back to designated datasets on EMBER. This labeler is restricted only to the standardized skeletons approved by the consortium.
  - Set up video tagging layer for admins.
  - Prototype annotation features for:
    - Event / behavior segmentation: 'subject is lost while navigating', 'happy facial expression', 'fidget'.
      - Can have two approaches: direct write-in and binary plurality consensus.
    - Spatial: centroid, bounding box, segmentation mask, 2D pose, 3D pose.
      - Centroids and segmentation masks will be the only items annotated directly; bounding boxes and assembled skeletons will merely be curated.
    - Proofreading / Curation: prediction X is wrong at frame Y in video Z (agnostic to annotation modality).
      - Will be done through matrix grid with hotkey tagging.
      - Will primarily source from inference outputs to fold in as 'confirmed' labels [with provenance maintained to distinguish from true directly annotated features].
  - In order to ensure consistent labeling practices, establish certification protocols for users per node type.
  - Enforce regular consistency checks over time for certified labelers to prevent stylistic drift.
  - Set up EMBER-HEARTH backend compute for model training per video, dataset, and model type (DLC/SLEAP/LP/etc.).
  - Automatically generate version-controlled inferences for each video for each trained model.
  - Create a dashboard for benchmarking and comparing model performance based on inference output.

### Phase 1b (March 2027)

- MILESTONE: Reach 1,000,000 labeled frames for single-subject, single-camera data available on EMBER.
- Assess the capabilities of one-shot transformers with this scale of training data.
- First official release of web-based platform.

### Phase 2 (June 2027)

- Expand data collection and foundation model training and inference to multi-subject, single-camera (top-down/bottom-up) cases while maintaining previous restrictions on field of view and environment.
  - May benefit from including new data annotation and model training for segmentation masks (outlines of subject) to help track and resolve animal identity.
- Analyze and prioritize frame labeling based on predicted information value (not necessarily uniform over time).
- Add capabilities to the platform for specialized use cases; pupil dilation, lick detection, breathing (only for qualifying field of views/resolutions).

### Phase 3 (December 2027)

- Expand data collection and foundation model training and inference to synchronized multi-camera cases while maintaining previous restrictions on the environment.
- Reach 2,000,000 labeled frames across all collections.

### Phase 4 (June 2028)

- Expand data collection and foundation model training and inference to multi-subject, multi-camera cases while maintaining previous restrictions on the environment.
- Reach 4,000,000 labeled frames across all collections, if the scaling laws for training have not yet saturated.

### Phase 5 (December 2028)

- Expand data collection and foundation model training and inference to non-caged (open) environments.
  - By its nature, this will include a variety of fields of view.
  - Start with single subject cases where possible and expand later to multi-subject.
- Reach 6,000,000 labeled frames across all collections, if the scaling laws for training have not yet saturated.

The hope is that phases 1-4 will make the extension to phase 5 relatively smooth.
