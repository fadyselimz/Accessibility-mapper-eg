# Accessibility Mapper (Egypt)

A computer-vision system that detects ramps, missing ramps, high curbs,
stairs with no accessible alternative, and blocked ramps from street
photos — then plots them on a map of accessible vs. inaccessible spots.

Egyptian cities have almost no structured data on physical accessibility.
This project's dataset, not just the model, is the original contribution.

## Approach
- Custom-trained YOLOv8 detector, 5 classes (see below)
- Base training data from small public curb-ramp / sidewalk datasets,
  fine-tuned on original street photos from Egypt
- Detections geotagged and plotted on an interactive map
- Served via FastAPI, with a Streamlit front end
- Containerized with Docker

## Classes
`ramp` · `no_ramp` · `high_curb` · `stairs_no_alt` · `blocked_ramp`

## Baseline (Day 1)
*Pretrained YOLOv8n on unlabeled street photos — what it gets right,
what it misses. Notes below once run.*

## Tech stack
Python · PyTorch · Ultralytics YOLOv8 · OpenCV · MLflow · FastAPI ·
Streamlit · Folium · Docker

## License
MIT