# 🍕 ML Request Success Prediction Challenge

**Goal:** Build a machine learning model to predict whether a user's request will be successful.

## 📁 Dataset Files

| File | Description |
|------|-------------|
| `data/train.json` | Training data with 3200 labeled examples |
| `data/test.json` | Test data with 800 examples (no labels) |

## 🎯 Task

1. Build a classifier using `data/train.json`
2. Predict labels for `data/test.json`
3. Submit your predictions in the format below

## 📤 Submission Format

Create a CSV file named `submission.csv` with exactly two columns:

```csv
hashed_id,prediction
abc123...,True
def456...,False
```

- `hashed_id`: The unique identifier from the test set
- `prediction`: Your predicted label (`True` = successful, `False` = unsuccessful)

See `sample_submission.csv` for an example format.

## 📊 Data Schema

Each row contains:

| Field | Type | Description |
|-------|------|-------------|
| `hashed_id` | string | Unique identifier for the request |
| `request_text_edit_aware` | string | Text content of the request |
| `request_title` | string | Title of the post |
| `requester_username` | string | Username |
| `requester_user_flair` | string | User badge/flair |
| `requester_account_age_in_days_at_request` | int | Account age when posting |
| `requester_upvotes_minus_downvotes_at_request` | int | Karma score |
| `requester_number_of_comments_at_request` | int | Total comments by user |
| `requester_number_of_posts_at_request` | int | Total posts by user |
| `requester_number_of_subreddits_at_request` | int | Number of communities user posted in |
| `requester_subreddits_at_request` | list | List of communities |
| `post_was_edited` | bool | Whether post was edited |
| `unix_timestamp_of_request` | int | Timestamp of request |
| `requester_received_pizza` | bool | **Target variable (train only)** |

## 📈 Evaluation

Your submission will be evaluated on:
- **Accuracy**: Primary metric
- **Precision/Recall/F1**: Secondary metrics

## ⚠️ Rules

1. Only use the provided dataset for training
2. Do not use external data sources to augment predictions
3. Submit only one `submission.csv` file

## 💡 Tips

- This is an NLP-heavy problem - the text fields contain valuable signal
- Class imbalance exists (~25% positive class)
- Feature engineering on user activity metrics can help

Good luck! 🚀
