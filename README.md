# Vehicle Recall Summarization and Retrieval System

## Overview
This project is a Python-based system designed to process vehicle recall data, retrieve relevant information based on a user's query, and summarize it using advanced language models. The system utilizes Hugging Face's LLaMA model for summarization and Sentence Transformers for document retrieval. It is optimized to run on a GPU to handle computationally intensive tasks efficiently.

---

## Key Features
1. Recall Data Preprocessing:
   - Filters dataset based on specific vehicle makes.
   - Combines description fields into a single summary for easier processing.

2. Document Retrieval:
   - Embedding-based system using Sentence Transformers.
   - Retrieves top-k most relevant documents based on user queries.

3. Summarization:
   - Summarizes retrieved documents using the `meta-llama/Llama-3.1-8B-Instruct` model.
   - Handles long inputs with truncation and beam search for optimal results.

4. GPU Utilization:
   - Leverages GPU resources to prevent crashes and improve performance.

---
## Example Input
   ```json
   {
       "make": "Ford",
       "model": "Escape",
       "year": "2001",
       "issue": "stuck throttle risk"
   }
   ```

---

## Example Output
### Retrieved Documents:
```
[
    ('02V117000', ' ON CERTAIN PASSENGER VEHICLES BUILT WITH MANUAL TRANSAXLES, ...', 0.45),
    ('02V266000', ' CERTAIN PASSENGER VEHICLES EQUIPPED WITH ADJUSTABLE PADELS, ...', 0.31),
    ...
]
```

### Summary:
```
ON CERTAIN PASSENGER VEHICLES BUILT WITH MANUAL TRANSAXLES, THERE IS THE POTENTIAL FOR THE SPEED CONTROL CABLE TO HANG UP AT THE THROTTLE BODY BRACKET...
```

Let me know if you'd like any adjustments! 🚀
