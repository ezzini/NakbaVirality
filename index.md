# AraSentEval 2026: A Shared Task on Sentiment Analysis and Swapping in Arabic

### Hosted with OSACT7 Workshop at LREC 2026

## 1. Overview of the Proposed Task
Sentiment analysis remains a cornerstone of Natural Language Processing (NLP), with critical applications ranging from social media monitoring to customer feedback analysis. While significant progress has been made, the Arabic language presents unique challenges due to its rich morphology and extensive dialectal variation. Most user-generated content, the primary source for sentiment data, is written in dialectal Arabic, which is often under-resourced and differs significantly from Modern Standard Arabic (MSA).

To address these challenges and foster innovation in Arabic NLP, we propose the Shared Task on Sentiment Analysis and Swapping in Arabic (SASA). This task is designed to move beyond standard sentiment classification by evaluating both the understanding and generation of sentiment in diverse Arabic contexts. SASA comprises two distinct but complementary subtasks:

*   **Subtask 1: Arabic Sentiment Swap**: A generative task where participants' systems must rewrite a given sentence to invert its sentiment polarity (e.g., positive to negative) while preserving its core meaning. This challenges models to go beyond surface-level cues and demonstrate a deeper grasp of semantics and syntax.
*   **Subtask 2: Arabic Dialect Sentiment Analysis**: A multi-class classification task focused on identifying the sentiment (positive, negative, or neutral) of texts written in various Arabic dialects. This subtask emphasizes the need for robust models that can handle the lexical and syntactic diversity of the Arab world.

## 2. Motivation for the Task
The motivation for SASA is twofold. First, there is a persistent need for high-quality benchmarks and models for Arabic dialect sentiment analysis. While previous shared tasks have addressed Arabic sentiment (El-Beltagy et al., 2017; Rosenthal et al., 2017), the dialectal aspect remains a significant hurdle. By providing a new, multi-dialect dataset, we aim to spur the development of models that are more effective on real-world, user-generated data.

Second, the field of Arabic NLP is mature enough to move towards more complex generative tasks. Sentiment swapping, a form of text style transfer, is a challenging NLG problem that has been explored in English (Shen et al., 2017) but remains largely untouched for Arabic. This is largely due to the scarcity of high-quality, parallel datasets required to train and robustly evaluate such models. Success in this task has direct applications in data augmentation, controlling the tone of conversational agents, and creative content generation. Subtask 1 pushes the community to develop models with more nuanced generative capabilities for Arabic.

By combining a classification task on diverse dialects with a challenging generative task, SASA will provide a comprehensive benchmark for sentiment understanding and manipulation in Arabic, fostering the development of more sophisticated and practically useful models.

## 3. Data/Resource Collection and Creation
The datasets for both subtasks are ready, having been collected and annotated.

*   **Subtask 1 (Sentiment Swap)**: The dataset for this task is MA’AKS (Mughaus et al., 2025), a manually-curated parallel dataset for Arabic text sentiment swap. It consists of 5,000 sentence pairs in Modern Standard Arabic where each pair consists of two sentences that share the same core topic but have opposite sentiment polarities (one positive, one negative). The data was curated from social media and news commentary and manually annotated and cross-validated to ensure high quality in terms of fluency, meaning preservation, and accurate sentiment inversion. The data will be split into training (4,000 pairs), development (500 pairs), and test (500 pairs) sets.
*   **Subtask 2 (Dialect Sentiment Analysis)**: The dataset for this task, Multi-Dialect-Sent (MDS-3), currently consists of 3,000 sentences annotated for 3-class sentiment (positive, negative, neutral). The dataset is balanced across five major dialects: Moroccan, Egyptian, Lebanese, and Saudi. The data was sourced from Hotel reviews, then translated and annotated by native speakers of each dialect.

**Current Status**: The core dataset is ready. We are in the process of expanding it to include more examples and potentially add two more dialects: Jordanian and Yemeni, to further increase the task's diversity and challenge before its official release.

## 4. Task Description
Participants can choose to participate in one or both subtasks. We will use the CodaLab platform for running both subtasks, which will handle submissions and host the official leaderboards.

### Subtask 1: Arabic Sentiment Swap
*   **Input**: An Arabic sentence and its source polarity (e.g., "هذا المطعم رائع للغاية", positive).
*   **Output**: A new Arabic sentence that preserves the core meaning of the input but expresses the opposite polarity (e.g., "هذا المطعم سيء للغاية").
*   **Evaluation**: The ranking will be based on the following automatic metrics:
    *   **Sentiment Style Accuracy**: A baseline sentiment classifier will be used to measure the percentage of outputs with the correct target polarity.
    *   **Content Preservation**: Semantic similarity will be measured using BERTScore (Zhang et al., 2019) between the input and output sentences.
    *   **Fluency**: Perplexity score calculated using a large Arabic language model.

### Subtask 2: Arabic Dialect Sentiment Analysis
*   **Input**: An Arabic sentence written in a specific dialect.
*   **Output**: A sentiment label from the set {positive, negative, neutral}.
*   **Evaluation**: Systems will be evaluated using standard classification metrics.
    *   **Primary Metric**: Macro F1-Score, to account for any potential class imbalance.
    *   **Secondary Metrics**: Overall accuracy, as well as precision, recall, and F1-score for each class.

## 5. Pilot Run Details
We conducted an internal pilot run for both subtasks to validate the datasets and evaluation methodology. For Subtask 1, the dataset was benchmarked using several state-of-the-art Large Language Models, including AceGPT, JAIS, and Llama-3. These models were evaluated in various settings (zero-shot, few-shot, and fine-tuning), confirming the dataset's quality and the task's feasibility. The pilot also highlighted the necessity of combining automatic metrics with human judgment for a fair assessment of NLG quality. For Subtask 2, an initial version of the dataset was verified in a recently organized shared task at RANLP '2025.

## 6. Tentative Timeline
We will adhere to the tentative timeline proposed by the OSACT7 organizers.

*   **December 15, 2025**: Release of training, dev data, and evaluation scripts.
*   **February 10, 2026**: Registration deadline and release of test data.
*   **February 17, 2026**: End of evaluation cycle (test set submission closes).
*   **February 24, 2026**: Final results released.
*   **March 10, 2026**: System description paper submissions due.
*   **March 20, 2026**: Notification of acceptance.
*   **March 30, 2026**: Camera-ready versions due.
*   **May 2026 (TBC)**: Main Conference (LREC 2026).

## Organizers
*   **Saad Ezzini**, King Fahd University of Petroleum and Minerals, KSA
*   **Paul Rayson**, Lancaster University, UK
*   **Shadi Abudalfa**, King Fahd University of Petroleum and Minerals, KSA
*   **Maram Alharbi**, Lancaster University, UK
*   **Mo El-Haj**, VinUniversity, Vietnam, Lancaster University, UK
*   **Samaher Alghamdi**, Lancaster University, UK
*   **Reem Alotaibi**, King Abdulaziz University, KSA
*   **Salmane Chafik**, UM6P, Morocco

## Participation Guidelines
*   For participation guidelines, please refer to [Participation Guidelines](guidelines.md).
*   Comprehensive instructions for preparing and submitting your paper(s) are available at [Paper Submission Guidelines](PAPER.md).

## References
*   Antoun, W., Baly, F., & Hajj, H. (2020). AraBERT: Transformer-based Model for Arabic Language Understanding. In Proceedings of the 4th Workshop on Open-Source Arabic Corpora and Processing Tools (OSACT), pages 9–15.
*   El-Beltagy, S. R., El Kalamawy, M., & Soliman, A. B. (2017). NileTMRG at SemEval-2017 Task 4: Arabic Sentiment Analysis. In Proceedings of the 11th International Workshop on Semantic Evaluation (SemEval-2017), pages 790–795.
*   Mughaus, R., Abudalfa, S., Luqman, H., Jibrin, F., Alali, M., Al-Dowayan, N., & Abdelali, A. (2025). MA’AKS: manually-curated parallel dataset for Arabic text sentiment swap. Language Resources and Evaluation.
*   Rosenthal, S., Farra, N., & Nakov, P. (2017). SemEval-2017 Task 4: Sentiment Analysis in Twitter. In Proceedings of the 11th International Workshop on Semantic Evaluation (SemEval-2017), pages 502–518.
*   Shen, T., Lei, T., Barzilay, R., & Jaakkola, T. (2017). Style Transfer from Non-Parallel Text by Cross-Alignment. In Advances in Neural Information Processing Systems 30.
*   Zhang, T., Kishore, V., Wu, F., Weinberger, K. Q., & Artzi, Y. (2020). BERTScore: Evaluating Text Generation with BERT. In Proceedings of the International Conference on Learning Representations.
