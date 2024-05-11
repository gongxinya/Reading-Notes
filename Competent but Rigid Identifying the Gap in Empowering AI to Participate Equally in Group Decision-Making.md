# Competent but Rigid: Identifying the Gap in Empowering AI to Participate Equally in Group Decision-Making

**CHI Conference on Human Factors in Computing Systems (CHI '23)**

# Abstract:

The article explores the role of Artificial Intelligence (AI) in group decision-making processes, especially in the context of human-AI collaborative decision-making. Although existing research has focused on the interaction between AI and individual decision-makers, there is limited understanding of AI's performance in group decision-making. The paper poses a research question: How does AI perform in group decision-making when it is given equal decision-making power to humans? To answer this question, the authors designed an experiment where two participants and an AI form a committee to rank three English essays.

# Method:

The study employed a "Wizard-of-Oz" research method, in which the AI was given equal discussion and voting rights with human members. The experimental task was to score and rank student essays, using the Nominal Group Technique (NGT) to structure the decision-making process. The AI's predictions and explanations were derived from a neural network-based Machine Learning (ML) model, while the AI's interaction with other group members was controlled by a human "wizard." The study recruited 20 English teachers from middle schools and universities in China, forming ten experimental groups to participate in the experiment.

**1\. Specific Application of the "Wizard-of-Oz" Research Method:**

- In this study, the "Wizard-of-Oz" method was used to simulate a scenario where a fully automated AI (named AESER) interacts with human participants. This approach allows researchers to explore and evaluate the role of AI in group decision-making, while the actual behavior of the AI is controlled by a hidden human operator (the "wizard").
- In the experiment, the AI communicated with human participants through a set of predefined rules, which limited the scope of the "wizard" to control the AI's ability to ask and answer questions. This design made the AI's behavior closer to what current AI technology can actually support, enhancing the authenticity of the study.

**2\. Group Decision-Making Process:**

- The group decision-making process was based on the Nominal Group Technique (NGT), a structured decision-making process that encourages equal contributions from all group members. NGT typically includes the following steps:
    
    - Step 1: Silent essay review, where each member independently reviews the given essays, provides trait scores, and proposes an essay ranking with clear arguments.
    - Step 2: Sharing of essay rankings, where members share their rankings and arguments with other members in random order.
    - Step 3: Group discussion, where members clarify their rankings through back-and-forth question-answering to address any confusion or differences in their proposed scores.
    - Step 4: Final voting, where members complete a questionnaire to suggest their final rankings separately, and the final group decision depends on the majority opinion.

**3\. Use of AI Model:**

- The AI model mentioned in the article is a neural network-based machine learning model used for Automated Essay Grading (AEG). The model is capable of calculating the overall score and four trait scores for each essay.
- This model was designed based on existing AEG research, using a pre-trained DistilBert layer for text embedding, and BiLSTM and linear layers to output trait scores. The model was trained using cross-validation and evaluated on a test set.

# Conclusion:

The study found that although the AI's perspective was considered valuable, it still played a secondary role in the group due to its inability to fully follow the dynamics of the discussion and make progressive contributions. Moreover, the participants' divergent opinions on an "equal AI" member shed light on the potential future of human-AI relations. While some participants supported the idea of AI sharing equal voting rights with humans, many others preferred that the final decision be primarily based on human will. The AI was deemed capable in scoring essays, but its interaction with participants was described as rigid, as participants needed a collaborator who could provide feedback on their opinions, answer their questions in depth, and raise critical questions to advance the group discussion process.

# Contributions:

- **Development of an AI model AESER that can participate equally in group decision-making with humans.** Through a constrained "Wizard-of-Oz" protocol, researchers designed the AI's interaction methods, enabling it to play a role in group decision-making.
- **Conduct of exploratory research,** with the participation of 20 English teachers, providing qualitative insights into how an AI group member collaborates with human experts to make decisions.
- **Reflection on the design of the AI group member,** offering perspectives on the future direction of AI in groups, especially in situations where AI shares decision-making power with humans.