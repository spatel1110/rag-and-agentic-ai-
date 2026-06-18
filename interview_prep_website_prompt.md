# MASTER PROMPT — RAG & Agentic AI Interview Prep Website

---

## COPY THIS ENTIRE PROMPT AND PASTE INTO YOUR AI MODEL

---

You are an expert full-stack developer and AI educator. Build me a **complete, single-file HTML website** that runs locally (just open `index.html` in browser — no server needed) for interview preparation on **RAG (Retrieval-Augmented Generation)** and **Agentic AI**.

---

## AUDIENCE & TONE

- Explain everything in **Hinglish** (mix of Hindi + English, like how Indian tech folks talk)
- Example tone: *"Bhai, RAG basically ek smart library hai jahan se LLM apna jawab dhundta hai — hallucinate nahi karta"*
- Keep it conversational, not textbook-style
- Use relatable Indian analogies where possible (Swiggy delivery boy = retrieval agent, etc.)

---

## TECH STACK (local, no server needed)

- **Single `index.html` file** — everything embedded (CSS + JS inline)
- **Tailwind CSS** via CDN: `https://cdn.tailwindcss.com`
- **Animate.css** via CDN for animations
- **Mermaid.js** via CDN for flow diagrams: `https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js`
- **Prism.js** via CDN for syntax-highlighted code blocks
- **Chart.js** via CDN for comparison charts
- **No React, no Node, no build tools** — pure HTML/CSS/JS
- Font: Google Fonts — **Inter** (body) + **JetBrains Mono** (code)

---

## WEBSITE STRUCTURE

### Navigation (sticky top navbar)
- Logo: "RAG & Agents 🤖" 
- Nav links: Home | RAG Basics | Advanced RAG | Agentic AI | Workflows | Interview Q&A | Cheatsheet
- Dark/Light mode toggle button

---

### PAGE SECTIONS TO BUILD

---

#### SECTION 1 — Hero
- Big headline: *"Kal Interview Hai? Koi baat nahi, hum hain na 🔥"*
- Subtext in Hinglish explaining what this site covers
- Animated typing effect showing: "RAG kya hai...", "Agentic AI kya hai...", "LangGraph kya karta hai..."
- Two CTA buttons: "RAG Start Karo" and "Agentic AI Dekho"

---

#### SECTION 2 — RAG Fundamentals

**2.1 RAG Kya Hai?**
- Hinglish explanation with analogy
- Animated Mermaid.js diagram showing: `User Query → Retriever → Vector DB → Context + Query → LLM → Answer`
- Comparison table (with icons):

| Approach | Cost | Accuracy | Freshness | When to Use |
|---|---|---|---|---|
| RAG | Low | High | Real-time | Dynamic knowledge |
| Fine-tuning | High | Very High | Stale | Domain-specific tone |
| Prompt Engineering | None | Medium | Stale | Simple tasks |

**2.2 RAG Ke Core Components**
- Cards layout (3 cards): Knowledge Base | Retriever | Generator
- Each card: icon + Hinglish explanation + code snippet

**2.3 Chunking Strategies**
- Visual diagram showing different chunk sizes
- Code example using LangChain RecursiveCharacterTextSplitter (Python, syntax highlighted)
- Animated comparison: small chunks vs large chunks — retrieval quality difference
- Table: chunk size recommendations by use case (128-256 for factoid, 256-512 for general, 512-1024 for complex)

**2.4 Embeddings**
- Visual: text → vector space animation (dots clustering)
- Distance metrics explanation: Cosine, Euclidean, Dot Product — with Chart.js bar chart showing trade-offs
- Code: OpenAI embeddings + Ollama embeddings example

**2.5 Vector Stores Comparison**
- Interactive comparison table with filter buttons (Free / Production / Self-hosted):

| Store | Type | Best For | Free Tier | Speed |
|---|---|---|---|---|
| Chroma | Embedded | Learning | Unlimited | Fast |
| FAISS | Library | High perf | Unlimited | Fastest |
| Qdrant | Server | Production | 1GB cloud | Fast |
| Pinecone | Managed | Zero-ops | 100K vectors | Fast |
| Milvus | Server | Billion-scale | Self-hosted | Fast |

---

#### SECTION 3 — Advanced RAG

**3.1 Retrieval Techniques** (tabbed interface):
- Tab 1: Basic Similarity Search — code + diagram
- Tab 2: MMR (Maximal Marginal Relevance) — animated diversity vs relevance slider visual
- Tab 3: Hybrid Search — BM25 + Dense vectors Mermaid diagram
- Tab 4: Contextual Compression — before/after visual

**3.2 Advanced Patterns** (accordion/expandable cards):

Each pattern: Hinglish explanation + Mermaid flow diagram + Python code snippet

- **RAG Fusion**: Multiple queries → RRF → Better recall
  ```
  Mermaid: Query → LLM generates 3 variations → Each hits VectorDB → Reciprocal Rank Fusion → Final Answer
  ```

- **HyDE (Hypothetical Document Embeddings)**: 
  ```
  Mermaid: Query → LLM generates hypothetical answer → Embed hypothetical → Search VectorDB → Real Answer
  ```

- **CRAG (Corrective RAG)**:
  ```
  Mermaid: Query → Retrieve → Grade relevance → [Relevant: Generate] OR [Not Relevant: Web Search → Generate]
  ```

- **Self-RAG**:
  ```
  Mermaid: Query → Should I retrieve? → Retrieve → Is this relevant? → Generate → Is this faithful? → Final Answer
  ```

- **Graph RAG**:
  ```
  Mermaid: PDF → Extract entities → Build Knowledge Graph (Neo4j) → Multi-hop Query → Answer
  ```

---

#### SECTION 4 — Agentic AI

**4.1 Agentic AI Kya Hota Hai?**
- Hinglish explanation: *"Bhai, RAG ek baar retrieve karta hai aur jawab deta hai. Agent? Woh sochta hai, plan banata hai, tools use karta hai, galti se seekhta hai — ek real employee ki tarah"*
- Animated comparison diagram:

```
RAG:     Query → Retrieve → Generate → Done ✓

Agent:   Query → Think → Plan → Tool Call → Observe → 
         Think again → Tool Call → Observe → Final Answer
```

**4.2 Agent Core Components**
- Visual architecture diagram (Mermaid):
```
Brain (LLM) → Memory (Short-term + Long-term) 
            → Tools (Search, Code, APIs, RAG)
            → Planning (ReAct / ToT)
            → Action → Observe → Loop
```

**4.3 Memory Systems**
Cards for each memory type:
- Short-term (conversation history)
- Long-term (vector DB persistent memory)
- Episodic (past task memory)
- Semantic (knowledge facts)

**4.4 Tool Use & Function Calling**
- Code example: defining a tool in LangChain
- Mermaid diagram: Agent decides which tool to call based on query
- Example tools list: Web search, Code executor, RAG retriever, Calculator, API caller

---

#### SECTION 5 — Agentic Workflows (LangGraph Focus)

**5.1 LangGraph Basics**
- Hinglish: *"LangGraph ek graph hai jahan nodes = functions, edges = decisions, state = shared memory"*
- Animated Mermaid diagram: State → Node1 → Conditional Edge → Node2 or Node3 → END

**5.2 Key Workflow Patterns** (each with Mermaid diagram + code):

- **ReAct Pattern**:
```
Mermaid: Input → Reason → Act (Tool) → Observe → Reason → Act → ... → Final Answer
```

- **Plan & Execute**:
```
Mermaid: Query → Planner (creates steps) → Executor (runs each step) → Replanner → Answer
```

- **Multi-Agent Supervisor**:
```
Mermaid: User → Supervisor Agent → [Research Agent | Code Agent | Analysis Agent] → Supervisor → Answer
```

- **CRAG with LangGraph**:
```
Mermaid: Query → retrieve_node → grade_documents → [relevant → generate] [not relevant → web_search → generate]
```

- **Self-RAG with LangGraph**:
```
Mermaid: Query → route_question → [vectorstore / web_search] → grade_documents → [generate / rewrite_query] → grade_hallucinations → [useful / not useful → rewrite]
```

**5.3 LangGraph Code Example**
Full working code block (syntax highlighted) for a simple ReAct agent with LangGraph:
- StateGraph definition
- Node functions
- Conditional edges
- Compilation and invocation

---

#### SECTION 6 — Interview Q&A

**Format**: Flashcard-style flip cards (click to reveal answer)

Include at least 20 Q&As covering:

RAG Questions:
1. RAG aur Fine-tuning mein kya difference hai?
2. Chunking strategy kaise choose karte hain?
3. MMR kya hai aur kab use karte hain?
4. Hybrid search kaise kaam karta hai?
5. HyDE pattern explain karo?
6. CRAG mein fallback mechanism kaise kaam karta hai?
7. Vector DB choose karne ke criteria kya hain?
8. Embedding model choose karne ka framework kya hai?
9. Parent Document Retriever kya hai?
10. Self-Query Retriever kaise kaam karta hai?

Agentic AI Questions:
11. RAG aur Agentic RAG mein kya difference hai?
12. ReAct pattern explain karo?
13. Agent memory types kaunse hote hain?
14. Multi-agent system mein supervisor pattern kaise kaam karta hai?
15. LangGraph mein state kya hota hai?
16. Tool calling kaise implement karte hain?
17. Agent evaluation kaise karte hain?
18. Human-in-the-loop kab zaruri hota hai?
19. Plan & Execute vs ReAct — kab kya use karein?
20. Graph RAG kab better hota hai vector RAG se?

Each answer: 3-4 lines in Hinglish, with key terms bolded.

---

#### SECTION 7 — Quick Cheatsheet

- Two-column layout: RAG Cheatsheet | Agentic AI Cheatsheet
- Each: key terms, formulas, code snippets, decision trees
- Print-friendly styling
- "Download as PDF" button (uses browser print)

---

## VISUAL DESIGN REQUIREMENTS

- **Dark theme by default** (toggle to light)
- Color palette:
  - Background: `#0f0f23` (dark) / `#f8fafc` (light)
  - Primary accent: `#6366f1` (indigo)
  - Secondary: `#22d3ee` (cyan)
  - Success: `#4ade80` (green)
  - Cards: `#1e1e3f` (dark) / `#ffffff` (light)
  - Code blocks: `#1a1a2e`
- Smooth scroll behavior
- Scroll-triggered fade-in animations for sections
- Hover effects on all cards (lift + glow)
- Progress bar at top showing scroll position
- Mobile responsive (works on phone too)

---

## CODE BLOCKS REQUIREMENTS

- Every code example must use **Prism.js** syntax highlighting
- Language: Python (for LangChain/LangGraph code)
- Include copy-to-clipboard button on each code block
- Show imports at top of every snippet
- Add inline comments in Hinglish: `# Yahan hum documents load kar rahe hain`

---

## MERMAID DIAGRAM REQUIREMENTS

- All workflow diagrams use Mermaid.js
- Style: dark theme matching site
- Every diagram has a title
- Use colors: 
  - Input nodes: `fill:#6366f1`
  - Process nodes: `fill:#1e1e3f`
  - Decision nodes: `fill:#f59e0b`
  - Output nodes: `fill:#4ade80`

---

## ANIMATIONS

- **Hero**: Typing animation for rotating text
- **Section entry**: Fade-up on scroll (Intersection Observer)
- **Diagrams**: Draw-on animation when diagram comes into view
- **Flip cards**: CSS 3D flip on click
- **Code blocks**: Slide-in from right
- **Progress bar**: Smooth fill on scroll

---

## DELIVERABLE

Produce **one complete `index.html` file** that:
1. Opens directly in Chrome/Firefox/Edge with no server
2. Has all CSS and JS inline or via CDN links
3. Is fully functional offline (except CDN resources)
4. Loads in under 3 seconds
5. Works on mobile screens (min 375px width)

**Start building now. Output the complete HTML file.**

---

## QUICK SETUP STEPS FOR LOCAL RUN

At the top of your response, also give me these 3 steps:
```
Step 1: Copy the HTML code
Step 2: Save as index.html on your Desktop
Step 3: Double-click to open in Chrome — Done! No npm, no server needed.
```

---
