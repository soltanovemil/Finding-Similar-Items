# Finding Similar Job Summaries Using MinHash and LSH

---

## Project Description
This project implements a scalable system to detect pairs of similar job summaries using the LinkedIn Jobs and Skills dataset. By leveraging advanced algorithms like MinHash and Locality-Sensitive Hashing (LSH), the project efficiently identifies job descriptions with high textual similarity. The solution focuses on handling large datasets, reducing computational complexity, and ensuring precise similarity evaluation.

### Key Features:
- Preprocessing of unstructured text data.
- Shingle generation for capturing local context.
- MinHash for dimensionality reduction.
- LSH for efficient candidate pair generation.
- Jaccard similarity for evaluating final similarity.

---

## Technologies and Libraries Used
- **Programming Language**: Python 3
- **Distributed Framework**: Apache Spark (PySpark)
- **Libraries**:
  - `numpy` for mathematical operations.
  - `matplotlib` for data visualization.
  - `re` for text preprocessing.
  - `pyspark.sql` for distributed data processing.

---

## Project Structure
1. **Preprocessing**:
   - Cleaned textual data to remove noise such as HTML tags, URLs, non-ASCII characters, numbers, and extra spaces.
   - Tokenized and removed stopwords to standardize the text.

2. **Shingle Generation**:
   - Generated 2-gram shingles from the preprocessed text to enhance context understanding.

3. **MinHash Signature Generation**:
   - Used MinHash to compute fixed-length signatures, approximating Jaccard similarity efficiently.

4. **Locality-Sensitive Hashing (LSH)**:
   - Partitioned MinHash signatures into bands for efficient candidate pair identification.

5. **Jaccard Similarity Evaluation**:
   - Evaluated the similarity of candidate pairs, retaining pairs with a similarity score above a predefined threshold.

6. **Visualization**:
   - Plots for frequent shingles, Jaccard similarity distribution, and probability of detecting similar items were generated.

---

## Setup Instructions
1. Clone this repository:
   ```bash
   git clone https://github.com/soltanovemil/Finding-Similar-Items.git
   cd Finding-Similar-Items

---

## Dataset
- **Name**: LinkedIn Jobs and Skills
- **Source**: [Kaggle: LinkedIn Jobs and Skills 2024](https://www.kaggle.com/datasets/asaniczka/1-3m-linkedin-jobs-and-skills-2024)
- **License**: ODC-By License, Version 1.0
- **Focus**: The `job_summary.csv` file and its `job_summary` column were analyzed.
