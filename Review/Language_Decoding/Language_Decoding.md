
A **brain-computer interface** that decodes continuous language from non-invasive recordings, like functional magnetic resonance imaging (fMRI) and electroencephalography (EEG), would have many scientific and practical applications. Currently, however, non-invasive language decoders can only identify stimuli from among a small set of words or phrases. 

<p align="center">
<img src="./Figure/Translating_the_brain.png" alt="Translating_the_brain" width="80%" style="display: block; margin: 0 auto"/>
</p>

---
## **A Review of Brain–Computer Interface-Based Language Decoding: From Signal Interpretation to Intelligent Communication**

<CENTER>Applied Sciences, 2025</CENTER>

<CENTER><i>University of Shanghai for Science and Technology</i></CENTER>

#### **一、核心内容概述**

本文系统回顾了BCI语言解码的演进，提出 **“解释-通信-互动”（ICI）三阶段发展架构**，强调认知神经科学与人工智能的交叉融合如何推动技术从基础信号分析迈向自然交互。文章重点分析了神经机制、计算模型及临床应用，并探讨了未来挑战与创新方向。

#### **二、ICI三阶段发展架构**

<p align="center">
<img src="./Figure/ICI.png" alt="ICI" width="80%" style="display: block; margin: 0 auto"/>
</p>

1. **信号解释阶段（基础阶段）**

   - ***技术特征***

	  - **单通道处理：** 聚焦局部脑区（如Broca区）的EEG/ECoG信号，依赖独立成分分析（ICA）和小波变换去噪。

      <p align="center">
      <img src="./Figure/broca_area.png" alt="broca_area" width="50%" style="display: block; margin: 0 auto"/>
      </p>

	  - **线性特征提取：** 主成分分析（PCA）、共空间模式（CSP）用于降维，提升信噪比.
      - **静态分类模型：** 支持向量机（SVM）、k-近邻（k-NN）主导，准确率约80%（如NIRS系统对ALS患者的二元指令识别）。

      <p align="center">
      <img src="./Figure/NIRS.png" alt="NIRS" width="30%" style="display: block; margin: 0 auto"/>
      </p>

   - ***应用场景***

     - 实验室环境下的简单指令分类（如“是/否”选择）。

     - 早期临床测试（如P300拼写器的字符选择任务）。

      <p align="center">
      <img src="./Figure/p300_speller.png" alt="p300_speller" width="80%" style="display: block; margin: 0 auto"/>
      </p>

   - ***局限性***

     - 依赖高信号质量，环境噪声易导致性能下降。

     - 模型跨用户泛化能力差，需频繁校准（如训练周期达5-7周）。

2. **动态通信阶段（高级阶段）**

   - ***技术突破***

     - **多模态融合：** 整合EEG（时间分辨率高）与fNIRS（空间分辨率高），提升语义解码鲁棒性。

      <p align="center">
      <img src="./Figure/NIRS.png" alt="NIRS" width="30%" style="display: block; margin: 0 auto"/>
      </p>

      <p align="center">
      <img src="./Figure/EEG_NIRS_framework.png" alt="EEG_NIRS_framework" width="80%" style="display: block; margin: 0 auto"/>
      </p>

     - **实时处理：** 自适应分类算法（动态SVM、在线学习）将延迟降至毫秒级（如2.64-10.23 ms）。
	     - Benchmarking of hardware-efficient real-time neural decoding in brain–computer interfaces:
		     - Local Decoding:

            <p align="center">
            <img src="./Figure/Local_decoding.png" alt="Local_decoding" width="70%" style="display: block; margin: 0 auto"/>
            </p>

		     - SNN Framwork:

            <p align="center">
            <img src="./Figure/SNN.png" alt="SNN" width="80%" style="display: block; margin: 0 auto"/>
            </p>

		     - LIF Neuron:

            <p align="center">
            <img src="./Figure/LIF.png" alt="LIF" width="100%" style="display: block; margin: 0 auto"/>
            </p>

		     - Experiment Setting:

            <p align="center">
            <img src="./Figure/Experiment_SNN.png" alt="Experiment_SNN" width="80%" style="display: block; margin: 0 auto"/>
            </p>

		     - Results:

            <p align="center">
            <img src="./Figure/Results_SNN_Memory.png" alt="Results_SNN_Memory" width="70%" style="display: block; margin: 0 auto"/>
            </p>

            <p align="center">
            <img src="./Figure/Results_SNN_Tradeoff.png" alt="Results_SNN_Tradeoff" width="60%" style="display: block; margin: 0 auto"/>
            </p>

     - **深度学习初步应用：** CNN提取时空特征，GRU/LSTM建模序列依赖。
	     - A Deep Learning Approach for Non-Invasive Alzheimer’s Monitoring Using Microwave Radar Data
			 - data preprocess pipeline:

        <p align="center">
        <img src="./Figure/datapreprocess_pipeline.png" alt="datapreprocess_pipeline" width="90%" style="display: block; margin: 0 auto"/>
        </p>

	     - EEGNet: A Compact Convolutional Neural Network for EEG-based Brain-Computer Interfaces
		     - Framework:

            <p align="center">
            <img src="./Figure/EEGNet.png" alt="EEGNet" width="90%" style="display: block; margin: 0 auto"/>
            </p>

		     - Results: 

            <p align="center">
            <img src="./Figure/Results_EEGNet.png" alt="Results_EEGNet" width="80%" style="display: block; margin: 0 auto"/>
            </p>

   - ***应用场景***

     - **连续语音解码：** ECoG信号解码实现每分钟10-15词的输出（如Herff等人“脑到文本”系统，错误率25%）。

      <p align="center">
      <img src="./Figure/brain_to_text.png" alt="brain_to_text" width="60%" style="display: block; margin: 0 auto"/>
      </p>

     - **情感交互：** 结合前额叶EEG与心率信号，识别用户情绪（如Li等研究，F1-score达0.85）。
	     - PSD Distribution:

        <p align="center">
        <img src="./Figure/emotional_comparsion.png" alt="emotional_comparsion" width="60%" style="display: block; margin: 0 auto"/>
        </p>

	     - Wave Frequency:

        <p align="center">
        <img src="./Figure/frequency_wave.png" alt="frequency_wave" width="50%" style="display: block; margin: 0 auto"/>
        </p>

	     - Emotional Wave:

        <p align="center">
        <img src="./Figure/emotional_wave.png" alt="emotional_wave" width="50%" style="display: block; margin: 0 auto"/>
        </p>

     - **临床突破：** ALS患者通过侵入式BCI实现基本沟通（McCane等研究，72%患者准确率超70%）。

   - ***典型案例***

     - Anumanchipalli团队利用ECoG信号合成语音，相关系数达0.69，首次实现无声发音的解码。
	     - Speech synthesis from neural decoding of spoken sentences:

        <p align="center">
        <img src="./Figure/ALS_speech.png" alt="ALS_speech" width="80%" style="display: block; margin: 0 auto"/>
        </p>

3. **智能互动阶段（创新阶段）**

   - ***技术前沿***

     - **端到端架构**：结合wav2vec 2.0预训练模型与对比学习（如Defossez等非侵入式系统，零样本解码未训练语句）。
	     - Decoding Speech Perception from Non-Invasive Brain Recordings:
		     - Model:

          <p align="center">
          <img src="./Figure/clip.png" alt="clip" width="70%" style="display: block; margin: 0 auto"/>
          </p>

     - **迁移学习**：跨用户模型迁移（如Wu等研究，训练时间从数周缩短至20分钟）。

   - ***应用场景***

     - **个性化语音合成：** Angrick团队通过植入式ECoG系统为ALS患者生成80%可懂语音，长期稳定性达6周。

      <p align="center">
      <img src="./Figure/Acoustic_speech_reconstruct.png" alt="Acoustic_speech_reconstruct" title="Overview of the closed-loop speech synthesizer. (**A**) Neural activity is acquired from a subset of 64 electrodes (highlighted in orange) from two 8 × 8 ECoG electrode arrays covering sensorimotor areas for face and tongue, and for upper limb regions. (**B**) The closed-loop speech synthesizer extracts high-gamma features to reveal speech-related neural correlates of attempted speech production and propagates each frame to a neural voice activity detection (nVAD) model (**C**) that identifies and extracts speech segments (**D**). When the participant finishes speaking a word, the nVAD model forwards the high-gamma activity of the whole extracted sequence to a bidirectional decoding model (**E**) which estimates acoustic features (**F**) that can be transformed into an acoustic speech signal. (**G**) The synthesized speech is played back as acoustic feedback." width="70%" style="display: block; margin: 0 auto"/>
      </p>

     - **多语言处理：** Chen等框架支持中英文混合解码，准确率差异小于5%。
	     - A neural speech decoding framework leveraging deep learning and speech synthesis:
		     - Decoder:

            <p align="center">
            <img src="./Figure/speech_ecog_decoder.png" alt="speech_ecog_decoder" title="**a**, The speech encoder architecture. We input a spectrogram into a network of temporal convolution layers and channel MLPs that produce speech parameters. **b**,**c**, The ECoG decoder (**c**) using the 3D ResNet architecture. We first use several temporal and spatial convolutional layers with residual connections and spatiotemporal pooling to generate downsampled latent features, and then use corresponding transposed temporal convolutional layers to upsample the features to the original temporal dimension. We then apply temporal convolution layers and channel MLPs to map the features to speech parameters, as shown in **b**. The non-causal version uses non-causal temporal convolution in each layer, whereas the causal version uses causal convolution. **d**, The ECoG decoder using the 3D Swin architecture. We use three or four stages of 3D Swin blocks with spatial-temporal attention (three blocks for LD and four blocks for HB) to extract the features from the ECoG signal. We then use the transposed versions of temporal convolution layers as in **c** to upsample the features. The resulting features are mapped to the speech parameters using the same structure as shown in **b**. Non-causal versions apply temporal attention to past, present and future tokens, whereas the causal version applies temporal attention only to past and present tokens. **e**, The ECoG decoder using LSTM layers. We use three LSTM layers and one layer of channel MLP to generate features. We then reuse the prediction layers in **b** to generate the corresponding speech parameters. The non-causal version employs bidirectional LSTM in each layer, whereas the causal version uses unidirectional LSTM." width="100%" style="display: block; margin: 0 auto"/>
            </p>

		     - Framework:

            <p align="center">
            <img src="./Figure/speech_decoding_framework.png" alt="speech_decoding_framework" title="The upper part shows the ECoG-to-speech decoding pipeline. The ECoG decoder generates time-varying speech parameters from ECoG signals. The speech synthesizer generates spectrograms from the speech parameters. A separate spectrogram inversion algorithm converts the spectrograms to speech waveforms. The lower part shows the speech-to-speech auto-encoder, which generates the guidance for the speech parameters to be produced by the ECoG decoder during its training. The speech encoder maps an input spectrogram to the speech parameters, which are then fed to the same speech synthesizer to reproduce the spectrogram. The speech encoder and a few learnable subject-specific parameters in the speech synthesizer are pre-trained using speech signals only. Only the upper part is needed to decode the speech from ECoG signals once the pipeline is trained." width="100%" style="display: block; margin: 0 auto"/>
            </p>

     - **脑控虚拟化身**：Metzger等系统结合语音解码与面部动作捕捉，实现实时表情同步（延迟<200 ms）。
	     - A high-performance neuroprosthesis for speech decoding and avatar control: 

        <p align="center">
        <img src="./Figure/multimodal_speech_decoding.png" alt="multimodal_speech_decoding" title="**a**, Overview of the speech-decoding pipeline. A brainstem-stroke survivor with anarthria was implanted with a 253-channel high-density ECoG array 18 years after injury. Neural activity was processed and used to train deep-learning models to predict phone probabilities, speech-sound features and articulatory gestures. These outputs were used to decode text, synthesize audible speech and animate a virtual avatar, respectively. **b**, A sagittal magnetic resonance imaging scan showing brainstem atrophy (in the bilateral pons; red arrow) resulting from stroke. **c**, Magnetic resonance imaging reconstruction of the participant’s brain overlaid with the locations of implanted electrodes. The ECoG array was implanted over the participant’s lateral cortex, centred on the central sulcus. **d**, Top: simple articulatory movements attempted by the participant. Middle: Electrode-activation maps demonstrating robust electrode tunings across articulators during attempted movements. Only the electrodes with the strongest responses (top 20%) are shown for each movement type. Colour indicates the magnitude of the average evoked HGA response with each type of movement. Bottom: _z_-scored trial-averaged evoked HGA responses with each movement type for each of the outlined electrodes in the electrode-activation maps. In each plot, each response trace shows mean ± standard error across trials and is aligned to the peak-activation time (_n_ = 130 trials for jaw open, _n_ = 260 trials each for lips forwards or back and tongue up or down)." width="80%" style="display: block; margin: 0 auto"/>
        </p>

#### **三、神经认知与计算基础**

1. **认知机制**

   - ***双通路模型***

      <p align="center">
      <img src="./Figure/dual_route_cascaded.png" alt="dual_route_cascaded" width="40%" style="display: block; margin: 0 auto"/>
      </p>

     - **词汇通路（背侧流）：** Broca区→顶叶，负责语音生成与句法处理（如θ波编码音节）。
     - **语音通路（腹侧流）：** Wernicke区→颞叶，支持语义理解（如γ波关联词汇整合）。

      <p align="center">
      <img src="./Figure/speech_dorsal_ventral_pathway.png" alt="speech_dorsal_ventral_pathway" width="60%" style="display: block; margin: 0 auto"/>
      </p>

   - ***工作记忆模型***

     - **中央执行系统：** 分配注意力资源，协调语音环（存储音素）与视空画板（处理文字视觉特征）。  
     - **情景缓冲器：** 整合长时记忆与实时语言信息，支持复杂句子理解。  

      <p align="center">
      <img src="./Figure/working_memory_model.png" alt="working_memory_model" width="40%" style="display: block; margin: 0 auto"/>
      </p>

   - ***注意机制***

     - **目标导向网络（背侧）：** 前额叶调控语言任务优先级。  
     - **刺激驱动网络（腹侧）：** 颞顶联合区响应突发语义冲突（如歧义词处理）。  

      <p align="center">
      <img src="./Figure/attention_mechanism.png" alt="attention_mechanism" title="Control of goal-directed and stimulus-driven attention in the brain" width="80%" style="display: block; margin: 0 auto"/>
      </p>

2. **神经基础**

   - ***关键脑区与网络***

     - **Broca区：** 左额下回，主导语法结构与发音计划（高频γ活动关联语音编码）。
     - **Wernicke区：** 左颞上回后部，语义整合中心（N400成分标志语义异常）。
     - **默认模式网络（DMN）：** 静息态下参与内部语言生成（如自我对话）。

   - ***时空动力学***

     - **神经振荡：** δ波（1-3 Hz）编码句子韵律，θ波（4-8 Hz）对应短语边界，γ波（>30 Hz）关联词汇检索。  
     - **事件相关电位（ERP）：** P300成分用于BCI拼写系统，N200反映早期语法错误检测。  

3. **计算方法**

   - ***特征提取技术***

     - **时空滤波：** CSP算法最大化类别间方差，适用于运动想象与语音意图分离。  
     - **深度学习模型：** EEGNet采用深度可分离卷积，参数量减少90%，准确率提升15%（Lawhern等）。  

   - ***分类算法演进***

     - **传统模型：** SVM在低维数据表现优异（准确率85%），但难以处理高维时序信号。  
     - **混合架构：** CNN+BiLSTM融合局部特征与长时依赖，语音解码错误率降低至30%以下。

   - ***评估体系***

     - **静态指标：** 准确率、F1-score（处理类别不平衡）。  
     - **动态指标：** 信息传输率（ITR）、跨会话一致性（如Angrick研究PCC>0.8）。  

#### **四、关键挑战与未来趋势**

1. **技术瓶颈**

   - ***信号质量*** 

	   - 肌电伪迹（EMG）与非稳态噪声（如眨眼）干扰显著，需发展自适应滤波（如独立向量分析，IVA）。

   - ***实时性限制***

	   - 高密度ECoG（256通道）数据处理延迟需压缩至50 ms以内，依赖边缘计算与神经形态芯片。

   - ***多模态融合难题***

	   - EEG-fNIRS时序对齐误差（约100 ms）影响语义解码，需动态时间规整（DTW）算法优化。

2. **临床转化挑战**

   - ***安全性*** 

	   - 侵入式BCI长期植入引发胶质增生风险（5年存活率<60%），需开发生物相容性涂层（如聚吡咯）。

   - ***伦理争议***

     - **隐私泄露：** 神经信号可能暴露潜意识思维，需联邦学习（FL）保护数据。  
     - **认知增强公平性：** 技术可能加剧教育资源分配不均，需政策引导。  

3. **未来方向**

   - ***技术融合***

     - **量子计算：** 优化大规模神经网络训练（如Grover算法加速特征搜索）。
     - **神经形态工程：** 脉冲神经网络（SNN）模拟生物突触，功耗降低10倍。

   - ***应用扩展***

     - **教育领域：** BCI辅助语言学习，实时监测注意力与记忆负荷。  
     - **元宇宙交互：** 脑控虚拟化身实现自然对话（如Meta的Project Cambria原型）。

   - ***标准化建设***

     - **数据协议：** 统一BCI数据格式（如BNCI Horizon 2030标准）。  
     - **临床评估框架：** 制定跨中心验证流程（如FDA的Breakthrough Device Program）。  

#### **五、结论**

BCI语言解码已实现从“信号到符号”的跨越，但距离自然交互仍需突破神经编码复杂性、系统鲁棒性与伦理壁垒。未来需聚焦 **“神经-算法-临床”三角协同**：
1. **神经机制**：探索语言网络的动态编码规律（如跨频段耦合）。  
2. **算法创新**：开发轻量化模型（如TinyML）与自监督学习框架。  
3. **临床落地**：推动BCI纳入医保体系，降低患者使用成本。  
最终，BCI有望重塑人机交互范式，为失语症、ALS等患者重建“语言自由”，并开启认知增强的新纪元。


- Willett et al. (2021), *Nature*：首次实现手写脑信号的文本解码。  
- Defossez et al. (2023), *Nat. Mach. Intell.*：非侵入式语音感知解码的端到端框架。  
- Chen et al. (2024), *Nat. Mach. Intell.*：ECoG驱动的个性化语音合成系统。

---
### **Semantic reconstruction of continuous language from noninvasive brain recordings**

<CENTER>Nature Neuroscience, 2023</CENTER>

<CENTER><i>The University of Texas at Austin</i></CENTER>

***Framework:***
<p align="center">
<img src="./Figure/Semantic_reconstruction_of_continuous_language_from_non-invasive_brain_recordings_framework.png" alt="Semantic_reconstruction_of_continuous_language_from_non-invasive_brain_recordings_framework" width="80%" style="display: block; margin: 0 auto"/>
</p>

***Result:***
<p align="center">
<img src="./Figure/Semantic_reconstruction_of_continuous_language_from_non-invasive_brain_recordings_result.png" alt="Semantic_reconstruction_of_continuous_language_from_non-invasive_brain_recordings_result" width="80%" style="display: block; margin: 0 auto"/>
</p>

---
