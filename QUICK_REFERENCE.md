# Quick Reference - Multi-Agent RAG System

## File Organization
```
📁 Conversational_AI/
├── 📓 Multi_Agent_RAG_System.ipynb       (MAIN NOTEBOOK - Run this)
├── 📄 IMPLEMENTATION_GUIDE.md             (Detailed step-by-step)
├── 📄 QUICK_REFERENCE.md                  (This file)
└── 📄 assignment2.docx                    (Original assignment)
```

---

## TASK BREAKDOWN

### Task 1: Document Processing & Indexing (2 marks)
**Time: 15 min | Code Cells: 10**
- DocumentProcessor: Ingests, cleans, normalizes documents
- 4 Indexing Strategies:
  - VectorIndex (semantic search via embeddings)
  - KeywordIndex (TF-IDF keyword matching)
  - GraphIndex (entity relationship graphs)
  - HybridIndex (combines all three via RRF)

### Task 2: Multi-Agent Collaboration (2 marks)
**Time: 15 min | Code Cells: 8**
- 5 Specialized Agents:
  - Policy Agent (compliance, governance)
  - Technical Agent (architecture, design)
  - Incident Agent (issues, resolutions)
  - Compliance Agent (security, privacy)
  - FAQ Agent (common questions)
- MultiAgentOrchestrator: Manages parallel retrieval, conflict detection, evidence unification

### Task 3: Evidence Verification (2 marks)
**Time: 15 min | Code Cells: 8**
- EvidenceVerificationPipeline:
  - Trust score = 40% confidence + 30% authority + 20% recency + 10% coherence
  - Duplicate detection (50% word overlap)
  - Re-ranking by trust
- ContextOptimizer:
  - Token estimation (4 chars per token)
  - Compression for long documents
  - Citation generation

### Task 4: Adaptive Retrieval (2 marks)
**Time: 15 min | Code Cells: 8**
- QueryClassifier: Categorizes into 6 types (FACTUAL, ANALYTICAL, COMPARATIVE, MULTI_HOP, SUMMARIZATION, RECOMMENDATION)
- QueryDecomposer: Splits complex queries
- AdaptiveRetrievalSystem: Planned retrieval, failure handling

### Task 5: Evaluation Framework (2 marks)
**Time: 20 min | Code Cells: 10**
- RetrievalEvaluator: Recall@k, Precision@k, MRR, nDCG, Coverage
- GenerationEvaluator: Hallucination detection, citation accuracy, completeness
- RobustnessTestSuite: 5 test categories
- ProductionMonitor: Dashboard metrics

---

## CLASS HIERARCHY

```
DocumentChunk ← DocumentMetadata
    ↓
DocumentProcessor
    ↓
┌─────────────────────────────────────┐
├── VectorIndex                        │
├── KeywordIndex                       │
├── GraphIndex                         │
└── HybridIndex (uses all three)       │
    ↓
RetrievalAgent (base class)
    ├── PolicyRetrievalAgent
    ├── TechnicalDocumentationAgent
    ├── IncidentAnalysisAgent
    ├── ComplianceAgent
    └── FAQAgent
    ↓
MultiAgentOrchestrator
    ↓
EvidenceVerificationPipeline
ContextOptimizer
    ↓
AdaptiveRetrievalSystem
    ├── QueryClassifier
    ├── QueryDecomposer
    └── (Orchestrator + Verifier + Optimizer)
    ↓
┌──────────────────────────────┐
├── RetrievalEvaluator          │
├── GenerationEvaluator         │
├── RobustnessTestSuite         │
└── ProductionMonitor           │
```

---

## KEY EXECUTION FLOW

```
1. SETUP
   └─ Install dependencies, import libraries

2. TASK 1: Indexing
   └─ Process documents → Build 4 indices → Test retrieval

3. TASK 2: Agents
   └─ Create 5 agents → Parallel retrieval → Conflict resolution

4. TASK 3: Verification
   └─ Verify evidence → Re-rank by trust → Compress context

5. TASK 4: Adaptation
   └─ Classify query → Decompose → Plan strategy → Execute

6. TASK 5: Evaluation
   └─ Retrieval metrics → Generation metrics → Robustness tests → Monitoring
```

---

## CRITICAL THRESHOLDS

| Component | Threshold | Action if Below |
|-----------|-----------|-----------------|
| Trust Score | > 0.50 | Evidence flagged for review |
| Confidence | > 0.70 | Request user clarification |
| Hallucination Score | < 0.50 | Add source verification |
| Citation Accuracy | > 0.90 | Re-verify citations |
| Recall@10 | > 0.70 | Expand search scope |
| Precision@5 | > 0.80 | Re-rank results |

---

## SAMPLE QUERIES TO TEST

```python
# Task 1: Simple retrieval
"database architecture and kubernetes configuration"

# Task 2: Multi-department
"What are security requirements and database access controls?"

# Task 3: Verify sources
"encryption standards for compliance"

# Task 4: Complex multi-hop
"Compare technical architecture requirements with security compliance standards and incident response procedures"

# Task 5: Challenging
"Tell me about non-existent features" (tests unanswerable)
```

---

## EXPECTED OUTPUTS

### Task 1
```
✓ Processed technical_manual.txt: 2 chunks
✓ Processed compliance_policy.txt: 2 chunks
✓ Processed incident_report.txt: 2 chunks
✓ Vector index built with 6 chunks
✓ Keyword index built with 6 chunks
✓ Graph index built with 24 nodes and 32 edges
Search Results Comparison: Vector vs Keyword vs Graph
```

### Task 2
```
[Policy Retrieval Agent] Retrieving...
  Retrieved 5 results
[Technical Documentation Agent] Retrieving...
  Retrieved 5 results
...
Total Evidence Items: 25
Unique Agents: 5
Contradictions Detected: 0-2
```

### Task 3
```
Evidence Verification Process:
Verified 25 evidence items
Trust Score: 0.600-0.950
Optimized Context Window:
- Evidence Items Included: 3-5
- Estimated Tokens: 1200-2000
- Compression Used: True/False
```

### Task 4
```
Query Classification: MULTI_HOP (confidence: 0.85)
Sub-queries: 2-3
Planned Agents: 3-5
Total Evidence Found: 5-15
Average Confidence: 0.65-0.85
```

### Task 5
```
Retrieval Metrics:
  Recall@5: 0.75
  Precision@5: 0.85
  MRR: 0.95
  nDCG@5: 0.88
Generation Metrics:
  Hallucination: No
  Citation Accuracy: 0.95
  Completeness: 0.85
Robustness Tests:
  Answerable: 2/2 ✓
  Unanswerable: 2/2 (correctly flagged)
  Multi-hop: 2/2 ✓
```

---

## IMPORTANT NOTES FOR VIRTUAL LAB

1. **Before Starting:**
   - Ensure Python 3.9+ is installed
   - Check available RAM (at least 4GB recommended)
   - Allow 30 minutes for first run (dependency installation)

2. **During Execution:**
   - Run cells sequentially, don't skip
   - Wait for each cell to complete before moving to next
   - Watch for warnings (safe to ignore most)
   - Check output after each cell

3. **Screenshot Checklist:**
   - [ ] Take full-screen screenshot after each task
   - [ ] Include cell output in screenshots
   - [ ] Show execution time indicators
   - [ ] Capture error messages (if any, note resolution)

4. **Common Issues:**
   - ImportError: Run dependency installation cell again
   - MemoryError: Close other applications, restart kernel
   - Empty results: Check sample documents are loaded

---

## MARKING BREAKDOWN (10 marks total)

**Task 1: Document Processing (2 marks)**
- ✓ 4 indexing strategies implemented: 0.5 marks each
- ✓ Metadata schema complete: 0.5 marks
- ✓ Comparison and analysis: 0.5 marks

**Task 2: Multi-Agent System (2 marks)**
- ✓ 5 specialized agents: 0.5 marks
- ✓ Orchestrator with collaboration: 0.75 marks
- ✓ Conflict resolution: 0.75 marks

**Task 3: Evidence Verification (2 marks)**
- ✓ Trust scoring (4 factors): 0.75 marks
- ✓ Context optimization & compression: 0.75 marks
- ✓ Citation generation: 0.5 marks

**Task 4: Adaptive Retrieval (2 marks)**
- ✓ Query classification (6 types): 0.5 marks
- ✓ Decomposition and planning: 0.75 marks
- ✓ Failure handling: 0.75 marks

**Task 5: Evaluation Framework (2 marks)**
- ✓ Retrieval metrics (5 types): 0.5 marks
- ✓ Generation metrics (4 types): 0.5 marks
- ✓ Robustness testing: 0.5 marks
- ✓ Monitoring dashboard: 0.5 marks

---

## FINAL CHECKLIST

- [ ] Clone/download notebook and guide files
- [ ] Open Jupyter in Virtual Lab
- [ ] Install all dependencies (Cell 1)
- [ ] Run all cells in sequence
- [ ] Take screenshots after each task
- [ ] Export notebook as PDF
- [ ] Create evaluation matrix document
- [ ] Compile all submission files
- [ ] Verify PDF contains all output
- [ ] Double-check all 5 tasks are complete

---

## ESTIMATED COMPLETION TIME

| Task | Execution | Documentation | Screenshots | Total |
|------|-----------|---------------|-------------|-------|
| 1 | 10 min | 5 min | 3 min | 18 min |
| 2 | 10 min | 5 min | 3 min | 18 min |
| 3 | 10 min | 5 min | 3 min | 18 min |
| 4 | 10 min | 5 min | 3 min | 18 min |
| 5 | 15 min | 5 min | 5 min | 25 min |
| **TOTAL** | | | | **~2 hours** |

---

## SUPPORT & RESOURCES

- Notebook has inline comments for every function
- Each task has "Expected Output" comments
- IMPLEMENTATION_GUIDE.md has detailed explanation
- All code is self-contained (no external APIs needed)
- Error messages are descriptive

**Good luck with your assignment!** 🚀
