This dataset contains 60 videos, recorded during a live Zoom session. During each video, we got one sample of data
from the encrypted traffic, and one sample of the video's parameters to infer the quality of the video, every five
seconds (overall, 12 samples per video). We combined this samples and created a dataset that indicated the video
quality during a Zoom session. based on the traffic conditions. We manually changed the traffic conditions, such as
limit bandwidth, adding latency or packet loss, in order to simulate different traffic conditions.

The features in the dataset, that we extracted from the encrypted traffic, are:

- Packets per second
- Destination port
- Source port
- Average time between packets
- Destination IP
- Bandwidth
- Packets length

The labels in the dataset, that infer the quality of the video , are:

- Resolution
- Frames per second
- Latancy
- Jitter
- NIQE - no-reference Video Quality Assessment (VQA) metric

In order to exract the features from the traffic in real-time, we used Pyshark- Python's dictionary that allows sniffing
packets from the traffic. In order to extract the labels from the Zoom session in real-time, we used Zoom's video SDK.
