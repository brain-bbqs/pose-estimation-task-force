# Pose Estimation Task Force

Placeholder repository for issues related to the pose estimation task force.



## Phase Plan

The mission of this project is quite extensive in scope.
As such, we are carefully planning each stage as limited, achievable steps, which will gradually accumulate the capabilities of the system.
We thus state the following milestones with expected deliverable dates and subtasks.

Dataset-specific RAG-style methods will be assessed and used throughout each phase.
Individual models will be trained per video and per dataset of consistent videos.
Mixtures of experts will be made across datasets.
Long-running cumulative models will be trained continuously over the entire collection.

### Phase 1 (December 2026)

- Collect a centralized collection of videos with top-down or bottom-up fixed camera field of views of caged rodents.
- Transcode all videos in the collection to a common physical or coordinate space.
- Work with the scientific community to define rigorous, well-documented, and anatomically justified standard skeleton definitions (at both coarse- and fine- levels of detail).
- Label 1,000,000 frames from the standard transcoding of the data collection using the standardized collection.
- Offer automatically generated ethogram methods from the inferred pose series for each model.
  - Ideally, also compare to some manually annotated ethograms for ground truth benchmark comparison.

### Phase 2 (June 2027)

- Expand data collection and foundation model training and inference to synchronized multi-camera cases while maintaining previous restrictions on the environment.
- Reach 2,000,000 labeled frames across all collections.
- Analyze and prioritize frame labeling based on predicted information value (not necessarily uniform over time).

### Phase 3 (December 2027)

- Expand data collection and foundation model training and inference to multi-subject single-camera (top-down/bottom-up) cases while maintaining previous restrictions on field of view and environment.
- Reach 3,000,000 labeled frames across all collections.

### Phase 4 (June 2028)

- Expand data collection and foundation model training and inference to multi-subject, multi-camera cases while maintaining previous restrictions on the environment.
- Reach 4,000,000 labeled frames across all collections.

### Phase 5 (December 2028)

- Expand data collection and foundation model training and inference to non-caged (open) environments.
  - By its nature, this will include a variety of fields of view.
  - Start with single subject cases where possible and expand later to multi-subject.
- Reach 5,000,000 labeled frames across all collections.

The hope is that phases 1-4 will make the extension to phase 5 relatively smooth.
