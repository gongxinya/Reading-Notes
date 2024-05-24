# **EmoWear: Exploring Emotional Teasers for Voice Message Interaction on Smartwatches**

**ACM CHI 2024**

# **Abstract**:

This study investigates a smartwatch voice messaging system called EmoWear, which allows users to apply 30 animated Emotional Teasers on message bubbles to reflect emotions. These teasers, based on semantic and acoustic processing, assist senders in choosing teasers based on emotional priority, thereby enhancing the emotional communication experience when receiving and sending messages.

# **Key Concepts**:

- Emotional Teasers: Provide a preview of the emotional tone of an awaiting message without revealing its content.
- Smartwatch: Serves as the research platform for sending and receiving voice messages.
- Animation: Used to express six basic categories of emotions (happiness, sadness, calmness, fear, surprise, and anger).

# **Research Background**:

Voice messages limit the shared emotional experience by not allowing the emotional tone to be judged before fully listening. EmoWear aims to improve this through Emotional Teasers.

# **System Design**:

- The EmoWear interface enables users to send or receive voice messages with Emotional Teasers.
- The backend algorithm integrates semantic and acoustic features to process input audio and outputs emotional classification results.
    
    1. **Emotion Classification Algorithm**: The backend algorithm is based on six emotional categories: happiness, anger, fear, surprise, sadness, and calmness.
    2. **Single-Modality Models**: The algorithm uses two pre-trained single-modality models to process text and speech data:
        
        - **Text-to-Emotion Model**: Utilizes Google's GoEmotion work, which categorizes emotions from textual content into 27 types and provides a correlation heatmap analysis to reveal a hierarchical structure of these emotions. Researchers mapped the relevant emotional labels back to the six emotional categories targeted by the EmoWear system and fine-tuned the BERT pre-training model using the converted 6-class GoEmotion dataset.
        - **Speech-to-Emotion Model**: Based on convolutional neural networks (CNN) and dense layers, using Mel-frequency Cepstral Coefficients (MFCC) as features for training. MFCC is widely used in speech recognition systems because it can represent the amplitude spectrum of the sound wave in a compact vector form.
    3. **Multimodal Fusion**: The text-based and speech-based probability results are fused at the decision level. Specifically, the fused probability $pfpf​$ is calculated using the formula: $pf=w1×ps+w2×ptpf​=w1​×ps​+w2​×pt​$, where $psps​$ and $ptpt​$ are the emotion prediction probabilities based on speech and text, respectively, and $w1w1​$ and $w2w2​$ are the fixed weights assigned to the speech and text modalities.
    4. **Model Training and Testing**: The RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) dataset was used to train the speech-to-emotion model, and the GoEmotion dataset was used to train the text-to-emotion model. Both models were trained and tested on their respective datasets.
    5. **Fusion Ratio**: By evaluating on the third-party multimodal emotion dataset MELD (Multimodal EmotionLines Dataset), the fusion model's weight ratio was determined. The ratio $w1:w2=1:2w1​:w2​=1:2$ provided the highest accuracy.
    6. **System Architecture**: The backend server, developed using Node.js, is responsible for processing input voice messages, generating emotion predictions, and relaying messages between senders and receivers.
- The interface rearranges the display order of emotional categories to prioritize two probable categories, simplifying the sender's selection.

# **User Process**:

1. **Recording Messages**: Users record voice messages on their smartwatches.
2. **Emotion Analysis**: The system automatically analyzes the voice messages to detect emotions.
3. **Selecting Emotional Teasers**: Based on emotion analysis, the system recommends and displays relevant animated emotional teasers.
4. **Sending Messages**: Users select an emotional teaser and send the voice message with the selected teaser.
5. **Receiving and Previewing**: The recipient sees the looping emotional teaser on their smartwatch, previewing the emotional tone of the message.
6. **Listening to Messages**: The recipient taps the emotional teaser to listen to the complete voice message.
7. **Replying Process**: If necessary, the recipient can record a reply and select their own emotional teaser.

# **User Study**:

- Mixed methods, including quantitative Likert scale questionnaires and qualitative semi-structured interviews.
- Compared the EmoWear system with the baseline system (using color-coded message bubbles as emotional cues).
- 24 participants (12 pairs) were evaluated, and the results showed that EmoWear significantly enhanced the emotional communication experience.

**1\. Sampling (Sampling)**

- **Target Group**: The study targets smartwatch users, especially those interested in voice message communication and emotional expression.
- **Sampling Method**: Snowball sampling was used, starting with recruitment through a college mailing list and relying on existing participants to recommend new potential participants.
- **Sample Size**: A total of 24 participants were recruited, forming 12 pairs.
- **Sample Diversity**: Participants included individuals of different genders, ages, and backgrounds to increase the representativeness and generalizability of the study results.

**2\. Experimentation (Experimentation)**

- **System Comparison**: The experiment compared the EmoWear system with the baseline system (using color-coded message bubbles as emotional cues).
- **Experimental Design**: The experiment used a paired and randomized design, with each pair of participants testing both the EmoWear and baseline systems.
- **Task Types**: Included both scripted conversations (Scripted Conversation) and unscripted conversations (Unstructured Conversation).
- **Experimental Process**: Participants first used one system to complete a series of tasks, then filled out a questionnaire, and then switched to the other system for the same process.

**3\. Measurement (Measurement)**

- **Quantitative Data**: Quantitative data were collected through Likert scale questionnaires, which included questions rating various aspects of the experience with emotional teasers.
- **Qualitative Data**: Qualitative data were collected through semi-structured interviews conducted after two rounds of testing to explore participants' experiences and insights in depth.
- **Data Analysis**: Questionnaire data were statistically analyzed using Wilcoxon signed-rank tests to assess differences between EmoWear and the baseline system.
- **Thematic Analysis**: Interviews were transcribed verbatim, and thematic analysis was applied to identify key themes and patterns, complementing the quantitative data and providing in-depth understanding.

# **Research Contribution**:

Provides a novel system and empirical knowledge regarding emotional teasers for voice messaging.

# **Key Findings**:

- EmoWear performed better in helping recipients predict and understand the sender's emotions.
- Senders believed that EmoWear's emotional teasers conveyed their emotions more clearly.
- Users felt that EmoWear enhanced the vitality, expressiveness, and interpersonal intimacy of communication.

# **Discussion and Future Work**:

- Suggests various possibilities and potential application scenarios for emotional teasers in future human-computer interaction design.
- Recommends that future research explore more emotional options, multi-emotion representation, user customization, integration of multiple information channels, and the incorporation of biosignals.

# **Conclusion**:

The EmoWear system provides users with a novel perspective to understand and enhance the emotional experience in voice message communication on smartwatches.

# **References（about Emotional Teasers）**:

1. **Chen et al. [12]**: This work utilized colored voice message bubbles to indicate different emotions, such as excitement, anger, sadness, and tranquility. It represents a pioneering exploration in adding emotional cues to voice messages on mobile phones.
2. **Aoki et al. [5]**: The EmoBalloon system conveyed the arousal level detected from text messages through generated explosion-shaped text bubbles. Although initially designed for text messages, this work demonstrated the potential of message bubbles as emotional teasers for voice messages.
3. **Hu et al. [43]**: They proposed a technique named Emojilization, a speech-to-text method that translates emotions from speech into emoji labels.
4. **Zhang et al. [13]**: They studied how the combination of text background color and typography could enhance the emotional and content delivery of speech-to-text systems.
5. **Oomori et al. [61]**: Implemented an emoji-based captioning system to support deaf or hard-of-hearing (DHH) individuals in voice-only meetings.
6. **Kim et al. [48]**: Visualized pitch and other subtle paralinguistic cues, using caption font elements to provide support for the deaf or hard-of-hearing community.
7. **de Lacerda Pataca et al. [20]**: Developed captioning techniques to convey the prosody and emotions of speech.
8. **Liu et al. [53, 54]**: Through the Animo and Significant Otter systems, they explored the use of abstract or intricate animations to share emotional states based on bio-data.