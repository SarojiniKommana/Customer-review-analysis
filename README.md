# Customer Review Analysis ⭐️

This project analyzes customer reviews using **VADER (Valence Aware Dictionary and sEntiment Reasoner)** to predict and convert textual feedback into star ratings. It simplifies understanding user sentiment and helps businesses gauge customer satisfaction effectively.

## 🔍 Overview

Text reviews can often be more informative than ratings, but not as easy to quantify. This project bridges that gap by:
- Taking in raw customer reviews.
- Analyzing the sentiment using the **VADER SentimentIntensityAnalyzer**.
- Mapping the sentiment score to a 1–5 star rating.
- Displaying the original review along with its predicted rating.

## 🛠️ Technologies Used

- **Python**
- **NLTK** (Natural Language Toolkit)
- **VADER Sentiment Analysis**
- **Pandas** & **NumPy** for data handling
- **Matplotlib / Seaborn** (optional: for visualizing results)

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/SarojiniKommana/Customer-review-analysis.git
cd Customer-review-analysis
````

### 2. Install Dependencies

```bash
pip install nltk pandas
```

And download VADER lexicon:

```python
import nltk
nltk.download('vader_lexicon')
```

### 3. Run the Script

```bash
python review_rating_predictor.py
```

## 🧠 How It Works

1. **Input**: A dataset or list of customer reviews (e.g., `"I loved the product!"`).
2. ### 📷 Sentiment Output Example

Below is a sample output table that showcases how **VADER sentiment analysis** responds to subtle changes in the input text:

![WhatsApp Image 2025-07-08 at 16 06 42_7fd47ddf](https://github.com/user-attachments/assets/805fa638-6f2f-40f3-9a6c-7ddded526d44)


#### 🔍 Explanation:

* This table shows **how variations in wording, punctuation, and emphasis** impact the sentiment scores.
* The input reviews are similar but differ in terms of added emphasis like capitalization (`VERY`), exclamation marks (`!`), and emojis (`:-)`).
* VADER detects the **intensity of sentiment** based on such cues and returns four key scores:

  * `neg`: Negative sentiment score
  * `neu`: Neutral sentiment score
  * `pos`: Positive sentiment score
  * `compound`: A normalized sentiment score between -1 and +1

#### 📌 Insight:

* The more expressive the review, the higher the **positive sentiment score** and **compound score**.
* For example:

  * `"This computer is a good deal."` → `compound: 0.44`
  * `"This computer is a VERY good deal!! :-)"` → `compound: 0.82`

This highlights the **effectiveness of VADER in understanding real-world user emotions** through simple text.



3. **VADER Sentiment Scoring**: Returns a compound score between -1 (most negative) and +1 (most positive).

4. **Rating Mapping**: Sentiment score is converted into a 1–5 star rating:

   * `compound ≤ -0.5` → ★☆☆☆☆ (1 star)
   * `-0.5 < compound ≤ 0` → ★★☆☆☆ (2 stars)
   * `0 < compound ≤ 0.3` → ★★★☆☆ (3 stars)
   * `0.3 < compound ≤ 0.6` → ★★★★☆ (4 stars)
   * `compound > 0.6` → ★★★★★ (5 stars)

5. **Output**: Displays the review and the predicted rating.

## 📊 Sample Output

```txt
Review: "The delivery was fast but the product was damaged."
Predicted Rating: 2 Stars
```

## ✅ Use Cases

* E-commerce platforms to auto-generate ratings from reviews.
* Review monitoring dashboards.
* Sentiment-based product/service improvements.


## 🙌 Contributions

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change or improve.

## Below screenshots shows Actual execution output of this project

![IMG-20250127-WA0013](https://github.com/user-attachments/assets/4162a90e-a131-4243-b641-ff10d5cf7b03)

![IMG-20250127-WA0012](https://github.com/user-attachments/assets/e7b18ca2-9b79-4eb0-9087-526f302d9cdc)

![IMG-20250127-WA0009](https://github.com/user-attachments/assets/3eca2a02-51b5-4e8b-af63-6f6e2191fc37)

![IMG-20250127-WA0008](https://github.com/user-attachments/assets/3f0a1334-bfe7-48f0-be44-c4f2639dc12b)

![IMG-20250127-WA0007](https://github.com/user-attachments/assets/1e01a59c-3f03-426d-a862-f7bacf568867)






---

