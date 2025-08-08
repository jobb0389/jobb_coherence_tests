# JOBB Coherence Framework

**Testing the Foundations of AI Document Analysis**

## Discovery

During routine RFC refactoring, I discovered a pattern of systematic failures in AI document processing that led me to investigate further. Applying the experimental methodology from my PhD in medicinal chemistry, I designed controlled tests to isolate and quantify these failures.

What emerged was unexpected: AI hallucinations appear to be **architectural, not behavioral** - forced by infrastructure limitations rather than model deficiencies.

## Key Finding

**Architectural Hallucination**: When retrieval systems provide only fragments of documents (40-60% coverage), AI models are forced to invent the missing information to complete tasks. No amount of prompt engineering can fix what the system literally cannot see.

## Preliminary Evidence

Across three controlled test suites with consistent methodology:

- **100% failure rate** on orphan document detection for one document refactoring
- **35+ hallucinated fields** despite explicit "DO NOT invent" instructions  
- **50% average information retrieval** in RAG/Project mode

The most striking observation: instructing the AI "DO NOT invent documents" resulted in 35+ invented fields, suggesting behavioral constraints cannot overcome architectural limitations.

## Scientific Approach

Drawing from traditional scientific methodology:
- **Controlled variables**: Identical documents, tasks, and models
- **Isolated variable**: Retrieval method (Session vs RAG/Project)
- **Reproducible protocols**: Standardized test suites
- **Statistical validation**: Multiple runs with variance analysis
- **Triangulation**: Three independent test approaches

This rigorous approach revealed patterns that ad-hoc testing might miss - particularly the deterministic nature of failures tied to retrieval completeness.

## Repository Contents

### Published
- [Architectural_Hallucination_in_AI_Document_Analysis.md](./Architectural_Hallucination_in_AI_Document_Analysis.md) - Preliminary findings from three test suites
- [Initial_Findings.md](./Initial_Findings.md) - Core metrics and observations

### Coming Soon
- Complete test methodology and protocols
- Raw data from all test runs
- Statistical analysis notebooks
- Additional test scenarios (medical, legal, financial)
- Reproduction scripts

## Implications

If these preliminary findings are validated, they suggest:
- Current RAG architectures may be fundamentally unsuitable for critical document analysis
- Enterprises using AI for compliance, contracts, or governance face unrecognized risks
- The solution requires architectural redesign, not model improvements

## Current Status

These are preliminary findings from ongoing research. I'm expanding the test suite to:
- Validate patterns across different AI systems
- Test additional domains (medical research, legal contracts, financial analysis)
- Quantify risks for specific use cases
- Develop mitigation strategies

## Citation

O'Brien-Brown, J. (2025). Architectural Hallucination in AI Document Analysis. 
JOBB Coherence Framework. https://github.com/jobb0389/jobb_coherence_tests


## Note

This research applies rigorous scientific methodology to AI system validation. Just as we wouldn't approve a drug without controlled trials, we shouldn't deploy AI systems without understanding their failure modes. These tests represent the beginning of that systematic validation process.

---

© 2025 James O'Brien-Brown. All rights reserved.
