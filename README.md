# CartoonCodec: Generative Talking Face Video Coding with Cartoon-Style Customization

## 1. Abstract

The rapid growth of video-based social applications has intensified the demand for efficient video transmission and personalized cartoon-style customization. Existing solutions typically apply talking face video codecs followed by cartoon-style control algorithms. However, the paradigm often leads to unsatisfactory compression performance and increased inference latency. To address these limitations, we propose CartoonCodec, a novel generative framework that unifies face video coding and cartoon-style control into an end-to-end process. Our framework encodes facial video sequences into compact motion feature representations, which are then compressed and transmitted alongside text prompts to achieve low-bitrate communication. To embed control into the coding process while ensuring efficient compression, a text-guided adaptive layer selection mechanism relying on compact facial representations is introduced to dynamically select and optimize the most influential layers in the generators.  In addition, a self-supervised domain adaptation training strategy is proposed to construct both multimodal and unimodal data pairs for the computation of diverse loss functions. This enables domain adaptation across the decoupled space. Extensive experimental results show that CartoonCodec outperforms baselines in compression efficiency across video reconstruction and cartoon-style control tasks while achieving the fastest encoding and decoding speeds. CartoonCodec provides key insights for advancing real-time face video communication with cartoon-style customization. 

## 2. Visual Comparisons on the Video Reconstruction and Cartoon-Style Control Tasks  (Similar Bit rates)

### 2.1 Visual Comparisons on the Video Reconstruction Task  (Similar Bit Rates)

To assess subjective quality in video reconstruction, we conduct comparisons between our proposed CartoonCodec scheme, the latest hybrid video coding standard (VVC), and four generative compression schemes (FOMM, FV2V, CFTE, and CTTR) at similar bit rates. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/dbd560be-8356-44a0-8dba-3dcd397406fd)](https://github.com/user-attachments/assets/dbd560be-8356-44a0-8dba-3dcd397406fd)

### 2.2 Visual Comparisons on the Cartoon-Style Control Task  (Similar Bit Rates)

To assess subjective quality in Cartoon-Style Control, we conduct comparisons between our proposed CartoonCodec scheme, VVC+DiffCLIP, VVC+NADA, VVC+DeltaEdit, and VVC+FRESCO at similar bit rates. Note that the cartoon-style control task includes five cases: Disney Princess, Pixar, Sketch, Zombie, and Anime Painting. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

#### Pixar Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/64a6b279-14b0-41e3-9728-5345c42b7357)](https://github.com/user-attachments/assets/64a6b279-14b0-41e3-9728-5345c42b7357)

#### Sketch Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/4ca4afc0-8df7-45fc-83bd-c042c0b7c1d6)](https://github.com/user-attachments/assets/4ca4afc0-8df7-45fc-83bd-c042c0b7c1d6)

#### Zombie Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/90d23741-3a1e-4d62-bd32-faaed6dbd7a7)](https://github.com/user-attachments/assets/90d23741-3a1e-4d62-bd32-faaed6dbd7a7)

#### Anime Painting Control Case (Similar Bit Rates)

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/7900be01-674c-449e-8387-4a3c43472550)](https://github.com/user-attachments/assets/7900be01-674c-449e-8387-4a3c43472550)

## 3. Visual results on the VoxCeleb testing dataset (Similar Bit Rates)

To assess our CartoonCodec scheme in more realistic scenarios, we selected testing sequences from the VoxCeleb dataset, an in-the-wild dataset that naturally includes complex background conditions. Specifically, we compare our CartoonCodec with VVC on the video reconstruction task at similar bit rates. In addition, we evaluate our CartoonCodec on the cartoon-style control task at similar bit rates. To facilitate clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/f676af32-c8d6-4c9b-8cda-4a5434755ea0)](https://github.com/user-attachments/assets/f676af32-c8d6-4c9b-8cda-4a5434755ea0)

## 4. Video demonstration of our CartoonCodec’s runtime performance

We provide a demonstration video of our CartoonCodec running on an NVIDIA A40 GPU with 48 GB of memory, showcasing the measurement process of encoding and decoding time of CartoonCodec. The video is available for download at https://github.com/xiaonae/CartoonCodec/releases/download/V1/A40_latest.mp4. The video includes the encoding and decoding of 10 testing sequences (108 frames each). The average encoding and decoding time per video is presented, which is consistent with the results in Table III of our response letter. That is, the total runtime on the encoding side is 5.86734 s, and the total runtime on the decoding side is 3.09567 s. In addition, three decompressed videos are randomly selected for playback. For this demonstration, Pixar is used as the target cartoon style. 

## 5. Visual results of our CartoonCodec on the cartoon-style control task (Fig. 10 of the initial manuscript)

To facilitate clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/2b86f149-3054-4f40-a83c-42c60dc46b0b)](https://github.com/user-attachments/assets/2b86f149-3054-4f40-a83c-42c60dc46b0b)

## 6. Visual results of the Ablation study

To analyze (1) the visual examples of three variants of our CartoonCodec scheme and (2) the disentangled poses and expressions of these variants on the Pixar control case, we present the following results. For clearer observation of the experimental results, the corresponding videos are provided in downloadable MP4 format.

[![IMAGE ALT TEXT](https://github.com/user-attachments/assets/bb4d0a57-627b-4d36-968e-2bdce0d6a2d3)](https://github.com/user-attachments/assets/bb4d0a57-627b-4d36-968e-2bdce0d6a2d3)










