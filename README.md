# EEG-Motor-Imagery

My project consists of my investigation of the two types of convolution utilized in Multi-Scale Hybrid Convolutional Neural Networks(MSHCNN). MSHCNN utilizes a one-dimensional convolution called 1DCNN to extract advanced temporal features of EEG signals, and a two-dimensional convolution called 2DCNN to extract temporal and spatial features of EEG signals(Tang X;Yang C;Sun X;Zou M;Wang H;, 2023).

In the paper, the novel methodology proposed by Yang, et. Al performed better than EEGNet on certain "Dataset A" which consists of EEG signals collected from 9 normal subjects during left-hand and right-hand motor imagery tasks. The data includes recordings from three channels (C3, C4, and Cz) across 5 sessions per subject. They also tested their methodology on "Dataset B" which consists of EEG data from 9 normal subjects performing four motor imagery tasks: left hand, right hand, feet, and tongue movements. Each subject participated in two sessions on different days, with each session consisting of 6 cycles. Dataset B is very similar to the BNCI2014001 dataset we have been tasked with. However, for their classification tasks, they took only the left-hand and right-hand motor imagery samples. Furthermore, majority of their reported results cover their model's performance on dataset A, and not B.

<div>
<img src="https://drive.google.com/uc?export=view&id=1VlbZ7vXGZi1meEa6YsjKMs-C9mnW6xdA" width="800"/>
</div>

I will be experimenting with the MSHCNN approach, but for all four types of samples: Left-hand, Right-hand, Foot, and Tongue, and comparing its performance with current state-of-the-art models such as EEGNet(Lawhern et al., 2018), and ShallowConvNet(Schirrmeister et al., 2018)

#### Intuition behind choosing MSHCNN

I chose MSHCNN because it reported great results(+90%) for the binary classification between left and right-hand motor imagery, and thought that its level of accuracy could be replicated, but for the complete classification, including tongue and feet

#### Dataset

http://moabb.neurotechx.com/docs/generated/moabb.datasets.BNCI2014_001.html#moabb.datasets.BNCI2014_001

The BNCI2014001 dataset contains EEG data from 9 different subjects. Each participant in the study were instructed to imagine performing specific motor tasks corresponding to different classes while their brain activity was recorded. 22 Ag/AgCl electrodes were used for that matter. The four motor imagery tasks are the following:

Image movement of the left hand (class 1)
Imagine movement of the right hand (class 2)
Imagine movement of both feet (class 3)
Imagine movement of the tongue (class 4)
Each subject participated in two sessions on two different days. Each session is comprised of 6 runs separated by short breaks. There are 12 trials for each of the four possible classes, for total of 48 trials in a singular run. Therefore, there are 288 trials per session.

During each trial, the subjects are sat in front of a computer screen. At the beginning of the trial, a fixation cross is displayed on the black screen accompanied by a short acoustic warning. After 2 seconds, the first cue in the form of an arrow points to one of the 4 imagery tasks. The cue remains on the screen for 1.25 seconds and the subjects are expected to perform the desired motor imagery task. The cue disappears after the 1.25 seconds and the cross is back on the screen, but the subjects should perform the motor imagery task for 4 seconds, until the cross is no longer displayed. It is important to mention that no feedback is provided during the experiment.

### Reference
https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10036384

Tang X, Yang C, Sun X, Zou M, Wang H. Motor Imagery EEG Decoding Based on Multi-scale Hybrid Networks and Feature Enhancement. IEEE Trans Neural Syst Rehabil Eng. 2023 Feb 3;PP. doi: 10.1109/TNSRE.2023.3242280. Epub ahead of print. PMID: 37022411.
