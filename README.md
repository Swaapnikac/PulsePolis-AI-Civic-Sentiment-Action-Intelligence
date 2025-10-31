# PulsePolis – AI Civic Sentiment & Action Intelligence

PulsePolis is an AI-powered civic intelligence prototype that listens to the public voice to help governments, nonprofits, and policymakers understand community sentiment and generate actionable, empathy-driven insights.

It analyzes anonymized, publicly available discussions (such as local Reddit threads, news comments, or city feedback portals) to detect emerging issues, measure public emotions, and synthesize policy-oriented recommendations — responsibly and transparently.

This project is inspired by the **Burnes Center for Social Change’s AI for Impact Program**, which promotes the ethical application of AI for civic innovation, human-centered governance, and equitable public service.

---

## Objectives
- Transform unstructured civic data into actionable policy intelligence  
- Detect early signals of public concerns through sentiment and topic analysis  
- Combine emotion understanding with generative AI insight synthesis  
- Promote transparency, inclusion, and empathy in AI-driven governance  

---

## Key Features
- **Civic Topic Detection:** Extracts key issues from public discussions  
- **Emotion & Sentiment Mapping:** Quantifies public emotion using NLP models  
- **LLM Insight Synthesis:** Generates empathy-based summaries and recommendations  
- **Bias & Transparency Layer:** Audits model responses using FAIR-Lens  
- **Interactive Dashboard:** Streamlit interface for visualization and exploration  

---

## Tech Stack
Python | OpenAI GPT-4 | LangChain | spaCy | TextBlob | Sentence-BERT | UMAP | HDBSCAN | Streamlit | pandas | scikit-learn  

---

## Workflow
1. Data is fetched from Reddit, RSS feeds, or sample civic discussion datasets.  
2. NLP preprocessing cleans and anonymizes text.  
3. Sentence embeddings cluster similar topics using **Sentence-BERT + UMAP + HDBSCAN**.  
4. Emotion and sentiment scores are generated for each cluster.  
5. GPT-4 synthesizes summaries and actionable recommendations.  
6. The system outputs a structured JSON “Civic Pulse Report” and visualization dashboard.  

---

## Ethical Design
- Uses only public, anonymized data  
- Strips all personal identifiers before processing  
- Integrates **FAIR-Lens** for bias, readability, and inclusion auditing  
- Ensures human oversight for all policy recommendations  

---

## Example Output

```json
{
  "topic": "Public Transportation in Boston",
  "dominant_emotion": "Frustration",
  "sentiment_score": -0.42,
  "top_issues": ["delays", "inaccessibility", "lack of updates"],
  "emerging_idea": "AI-driven bus tracking for low-vision riders",
  "summary": "Residents express consistent frustration with transit delays and communication gaps. Sentiment trends show increasing concern about accessibility. An AI-powered rider notification system could improve trust and transparency.",
  "equity_note": "Prioritize accessibility for elderly and disabled riders in low-income areas."
}
