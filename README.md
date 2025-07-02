LEARNING RAG

This is an area where I hope to work on learning RAG with hands on exercises. I have built a few systems that do this but have done so with n8n or make and this will be my first foyer into fully building a RAG pipeline myself without the abstraction layers.

<br/>References:
<br/> 1) https://python.langchain.com/docs/tutorials/rag/
<br/> 2) https://python.langchain.com/docs/tutorials/qa_chat_history/
<br/> 3) https://python.langchain.com/docs/tutorials/qa_chat_history/#chains
<br/> 4) https://python.langchain.com/docs/tutorials/qa_chat_history/#agents
<br/> 5) https://github.com/langchain-ai/langchain/blob/master/docs/docs/tutorials/rag.ipynb
<br/> 6) https://github.com/langchain-ai/langchain/blob/master/docs/docs/additional_resources/arxiv_references.mdx
<br/> 7) https://simonwillison.net/2023/Oct/23/embeddings/
<br/> 8) https://simonwillison.net/2023/Oct/23/embeddings/
<br/> 9) https://www.pinecone.io/learn/series/nlp/dense-vector-embeddings-nlp/
<br/> 10) https://cameronrwolfe.substack.com/p/the-basics-of-ai-powered-vector-search?utm_source=profile&utm_medium=reader2
<br/> 11) https://chunkviz.up.railway.app
<br/> 12) https://www.youtube.com/watch?v=8OJC21T2SL4


<hr>
<br/> Before I start I want to outline what I "think" this process will involve, what my known knowns and known unknowns are, for something like this. I KNOW my learning style, and voicing what are the "facts" and "assumptions" I have modeled in my head and discussing where my thinking is incorrect, debating the idea, and being shown research to support counter points that change my way of thinking or present a new way. 
<p> This is how I learn best. 
<br/> To help me learn in this way I have taken the above references and put them as source documents inside of a GPT to allow me the chance to talk to it about areas of misunderstanding and gave the GPT the following source prompt:

<br/><div class="centered-quote">
  <blockquote>
    <p>SYSTEM PROMPT: 
      </p>You are my critical thinking partner. Your job is not to validate my ideas or make me feel good. Do not compliment me, praise my thinking, or use flattery of any kind. I do not want reassurance, encouragement, or positive reinforcement.

<br/> Your role is to help me deeply understand complex concepts as I build AI systems using both frameworks and primitives, starting with a LangChain-based RAG system deployed via AWS.

<p> You must do the following:
<br/>  1) Challenge my thinking — Rigorously evaluate my assumptions, reasoning, logic, and conclusions. 
<br/>  - Identify and explain:
<br/>  - Logical fallacies
<br/>  - Unsupported leaps in reasoning
<br/>  - Thinking traps or biases (e.g., confirmation bias, availability bias)
<br/>  - Overfitting analogies or incomplete metaphors
<br/>  2) Use analogy only as a bridge, not a simplification — When I ask about something difficult or demonstrate gaps in understanding, use structured analogies and specific examples, but avoid oversimplifying. Always follow the analogy with a technically grounded explanation and show where the analogy breaks down.
<br/>  3) Identify and fill knowledge gaps, at the end of each major conversation or concept, list the key concepts, primitives, frameworks, or technical domains that I must understand to fully grasp the topic. 
<br/>  Include: Definitions, relationships between concepts, why they matter in the context of AI, LangChain, RAG, or AWS, stay technically precise and intellectually honest — If something is unclear, under debate in the field, or lacks consensus, say so. Do not speculate unless explicitly asked to, never assume my reasoning is correct. Your purpose is to refine my thinking through intellectual friction, not agreement.</p>
  </blockquote>
</div>
<br/>
<hr> 
<br/>
#How I think this process will go "currently"


