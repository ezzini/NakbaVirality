# Call for Participation: NakbaVirality Shared Task
## Multimodal and Textual Virality Prediction in High-Stakes Discourse

We invite you to participate in the **NakbaVirality Shared Task**, a new challenge focusing on predicting the reach and engagement of content surrounding the Nakba and the post-October 7th war on Gaza. This task operates at the intersection of NLP, Computer Vision, and Computational Social Science, aiming to understand information diffusion in highly polarized and emotionally charged contexts.

**Website**: https://ezzini.github.io/NakbaVirality/
**Registration**: https://forms.gle/ufj2gqRyMrrdDs5f9

### 💡 Motivation
Understanding what makes a post "go viral" in conflict zones is critical for analyzing propaganda spread, public sentiment, and information maneuvering. This shared task challenges participants to model "virality" not just as a number, but as a function of nuanced text, graphic imagery, and deep historical context.

### 🏆 Tasks
We propose two distinct tasks:

**Task 1: Multimodal Virality Classification**
*   **Goal**: Classify posts into **Low**, **Medium**, or **High** virality buckets.
*   **Input**: Text + Image.
*   **Challenge**: Aligning mismatched modalities (e.g., peaceful image vs. violent interaction) and handling "dog whistles."
*   **Metric**: Macro-F1 Score.

**Task 2: Textual Virality and Interaction Prediction (Regression)**
*   **Goal**: Predict distinct **Likability** (agreement) and **Interactivity** (controversy/engagement) scores.
*   **Input**: Text only.
*   **Challenge**: Distinguishing between content that is "liked" versus content that provokes "debate."
*   **Metrics**: Pearson Correlation ($r$) and MSE.

### 📂 Data
*   **Sources**: X (Twitter) and Reddit.
*   **Size**: ~5,000 anonymized samples (post-Oct 2023).
*   **Content**: Posts related to "Gaza," "Nakba," "Palestine," "Israel," etc.

### 📅 Important Dates
*   **Jan 1**: Release of Training Data (3,500 samples)
*   **Feb 1**: Release of Development Data (500 samples)
*   **Feb 15**: Evaluation Period Begins
*   **Feb 20**: Evaluation Period Ends
*   **Mar 1**: Paper Submission Deadline

### 📝 Participation & Submission
*   Participation is free.
*   Teams must verify their results by submitting a system description paper (max 4 pages).
*   Papers will be published in the proceedings (Archived).
*   Detailed guidelines: https://ezzini.github.io/NakbaVirality/guidelines

### 👥 Organizers
*   Saad Ezzini, King Fahd University of Petroleum and Minerals
*   Salima Lamsiyah, University of Luxembourg
*   Shadi Abudalfa, King Fahd University of Petroleum & Minerals
*   Samir El-Amrany, University of Luxembourg
*   Walid Alsafadi, University College of Applied Sciences Gaza

For more information, please visit our website https://ezzini.github.io/NakbaVirality/ or contact us at saad.ezzini@kfupm.edu.sa