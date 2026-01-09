# NakbaVirality: Multimodal and Textual Virality Prediction in High-Stakes Discourse

### Hosted with NakbaNLP Workshop at LREC 2026

## 1. Motivation and Introduction
Social media has become the primary battleground for narrative control during geopolitical conflicts. The discourse surrounding the Nakba and the post-October 7th war on Gaza represents a unique intersection of historical trauma, real-time war reporting, and highly polarized sentiment.

Understanding what makes a post "go viral" in this specific context is critical for analyzing information diffusion, propaganda spread, and public sentiment. This shared task proposes a novel challenge: predicting the reach (virality) and engagement (interaction) of posts where the content is emotionally charged, historically deep, and often multimodal (text combined with graphic or symbolic imagery).

By focusing on this specific domain, we aim to push the boundaries of how NLP and Computer Vision models handle context-heavy, sensitive, and polarizing data.

## 2. Data Description
We present a curated, multi-platform dataset specifically designed for this task.

*   **Data Sources**: X (formerly Twitter) and Reddit.
*   **Dataset Size**: Around 2,600 distinct samples.
*   **Languages**: Mostly English (60%) and Arabic (10%), with others including Farsi, Hebrew, Spanish, Turkish, etc.
*   **Scope**: Content published post-October 7th, 2023, filtered using keywords related to "Gaza," "Nakba," "Palestine," "Israel," and specific conflict-related terminology.
*   **Data Fields**:
    *   **Text**: The raw post content (caption/tweet).
    *   **Visual**: The associated image or video thumbnail.
    *   **Metadata**: Timestamp, user follower count (for normalization).
    *   **Ground Truth Labels**: Like count, Share/Retweet count, Comment count.

**Note on Ethics**: All data will be anonymized to protect user privacy, given the sensitive nature of the topic. IDs and handles will be hashed.

## 3. Task Definition
We propose a single task to evaluate model performance on multimodal virality prediction.

### Multimodal Virality Classification
This task focuses on the interplay between text and imagery. In conflict zones, an image often determines the spread of a post more than the text.

*   **Input**: Post Text + Post Image.
*   **Objective**: Classify the social media post (text and image) into three virality classes based on a normalized "impact score" (derived from likes and shares).
*   **Classes**:
    *   **Low Virality**: Content with minimal reach.
    *   **Medium Virality**: Content with average engagement.
    *   **High Virality**: "Viral" content.
*   **Evaluation Metric**: Macro-F1 Score (to account for potential class imbalance).

## 4. Baseline Systems
To assist participants, the organizers will provide the following baseline:

*   A late-fusion architecture using BERT (for text) and ResNet-50 (for images), concatenated into a softmax classifier.

## 5. Significance and Impact
This shared task contributes to the NLP community by:

*   **Contextual Modeling**: Testing how models handle "dog whistles" and specific historical references (Nakba) that require external knowledge.
*   **Cross-Platform Analysis**: Comparing virality features between X (short-form, immediate) and Reddit (community-based, threaded).
*   **Multimodal Alignment**: Understanding how mismatched modalities (e.g., a peaceful image with violent text) affect virality in conflict scenarios.

## 6. Tentative Schedule
*   **Jan 1**: Call for Participation. 
*   **Jan 10**: Release of Training Data (1,800 samples).
*   **Feb 10**: Evaluation Period Begins (Test set: 900 blinded samples)
*   **Feb 17**: Evaluation Period Ends.
*   **Feb 21**: Release of Results.
*   **Mar 1**: Paper Submission Deadline.

## 7. Organizers

*   Saad Ezzini, King Fahd University of Petroleum and Minerals
*   Salima Lamsiyah, University of Luxembourg
*   Shadi Abudalfa, King Fahd University of Petroleum & Minerals
*   Samir El-Amrany, University of Luxembourg
*   Walid Alsafadi, University College of Applied Sciences

## Participation Guidelines
*   For participation guidelines, please refer to [Participation Guidelines](guidelines.md).
*   Comprehensive instructions for preparing and submitting your paper(s) are available at [Paper Submission Guidelines](PAPER.md).
