<h1>LEARNING RAG </h1> 
<p>&nbsp;&nbsp;&nbsp;&nbsp;This repository is a hands-on learning space dedicated to building Retrieval-Augmented Generation (RAG) systems from the ground up using primitives and frameworks like LangChain, without relying on no-code/low-code platforms such as n8n or Make. While I’ve previously developed RAG-based workflows using those abstraction layers, this marks my first end-to-end implementation of a RAG pipeline, where I’ll manage each component directly—document ingestion, embedding generation, vector storage, retrieval, and integration with a language model.</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;The goal is not just to build something that works, but to deeply understand how each layer of a RAG system functions and interacts. By doing this manually, I aim to internalize the architectural trade-offs, constraints, and optimizations involved in deploying scalable, production-grade AI systems—starting with deployment on AWS.</p>
<hr>
<h2>References:</h2>
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
<h2>HOW I INTEND TO LEARN USING THIS REPO</h2>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Before I start I want to outline what I "think" this process will involve, what my known knowns and known unknowns are, for something like this. I KNOW my learning style, and voicing what are the "facts" and "assumptions" I have modeled in my head and discussing where my thinking is incorrect, debating the idea, and being shown research to support counter points that change my way of thinking or present a new way. </p>
<p><h1>This is how I learn best.</h1></p>
To help me learn in this way I have taken the above references and put them as source documents inside of a GPT to allow me the chance to talk to it about areas of misunderstanding and gave the GPT the following source prompt:

<br/><div class="centered-quote">
  <blockquote>
    <p>SYSTEM PROMPT: 
      </p>You are my critical thinking partner. Your job is not to validate my ideas or make me feel good. Do not compliment me, praise my thinking, or use flattery of any kind. I do not want reassurance, encouragement, or positive reinforcement.

<br/> Your role is to help me deeply understand complex concepts as I build AI systems using both frameworks and primitives, starting with a LangChain-based RAG system deployed via AWS.

<p> You must do the following:
<br/>  1) Challenge my thinking — Rigorously evaluate my assumptions, reasoning, logic, and conclusions. 
<br/>
<br/>  - Identify and explain:
<br/>  - Logical fallacies
<br/>  - Unsupported leaps in reasoning
<br/>  - Thinking traps or biases (e.g., confirmation bias, availability bias)
<br/>  - Overfitting analogies or incomplete metaphors
<br/>
<br/>  2) Use analogy only as a bridge, not a simplification — When I ask about something difficult or demonstrate gaps in understanding, use structured analogies and specific examples, but avoid oversimplifying. Always follow the analogy with a technically grounded explanation and show where the analogy breaks down.
<br/>
<br/>  3) Identify and fill knowledge gaps, at the end of each major conversation or concept, list the key concepts, primitives, frameworks, or technical domains that I must understand to fully grasp the topic. 
<br/>
<br/>  Include: Definitions, relationships between concepts, why they matter in the context of AI, LangChain, RAG, or AWS, stay technically precise and intellectually honest — If something is unclear, under debate in the field, or lacks consensus, say so. Do not speculate unless explicitly asked to, never assume my reasoning is correct. Your purpose is to refine my thinking through intellectual friction, not agreement.</p>
  </blockquote>
</div>
<br/>
<hr> 
<h2>WHAT I THINK THE STEPS ARE "CURRENTLY"</h2>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Below is a list of the steps I believe I will need to complete before I watch any of the content. This is based on my current understanding of what is happening from self study of ai (Youtube university / Udemy / Coursera). Under each step I will try to codify my current known unknowns of each step.</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Additionally I am going to give a triple numeric confidence score for each step (10,10,10). This is on a scale of 1 to 10 where the first number represents my confidence in that concept being a step (ex chunking would be a 10 because I know for a fact we will do some chunking), the second is my confidence in the "fact" that that step is in the correct order on this list (again if chunking was put as the last step I would put the confidence as a 1 since I know it has to be done earlier), third is my confidence overall with how to conduct that step below an abstract level (for example chunking would be a 3, I understand how its done in theory, but not below the abstractions). </p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;All of this is in the hopes of quantifying my understanding and comparing my current conceptual understanding to an end assessment once I have finished the tutorial. I want to understand where I am in regards to the dunning-kruger effect curve (hopefully not still climbing mount stupid) 
  NOTE: If the step below is italic then its not a step specific to rag but instad is just an IMO on what are best practices when doing any projects.</p>
<br/> *STEP 1: Figure out what I want to build... Ideate on 5-10 problems (not solutions) dont worry if AI is the best solution, get problems listed before you think about solutions*
<br/> 
<br/> *STEP 2: Match a potential solution to the problem (again dont worry about using AI but list all the ways you would solve that problem.* 
<br/> 
<br/> *STEP 3: Optimize the solution: here is where you can figure out which of those solutions is a MUCH better solution if you infuse AI into the solution*
<br/> 
<br/> STEP 4: Gather documents and data to go into the RAG pipeline for the LLM to draw from.
<br/> 
<br/> STEP 5: Chunk the documents/data/reference material
<br/> 
<br/> STEP 6: Embed it or give it an Embedding (give it a numerical representation that allows it to sit in 3D space inside of a Vector data base
<br/> 
<br/> STEP 7: Build the vector database of Embeddings
<br/> 
<br/> STEP 8: Build a retrieval system that can look for the relevant references inside the vector data base
<br/> 
<br/> STEP 9: Evaluate which LLM would be the best fit for your use case. 
<br/> 
<br/> STEP 10: Build the required system prompts for the model based on the use case, and do a prompt evaluation loop to make sure the prompts are generating the correct outputs.
<br/> 
<br/> STEP 11: Connect the pipeline to the model

<h1>Analogy</h1>
<p>I like to work in analogies and here is the analogy I have thought of for RAG "right now" before I begin to do the langchain tutorial. Imagine you are a mother and you are making a dessert which is a bunch of fruit cut up and put into green jello. If you mix it all together you will have a random assortment of fruit throughout the whole jello mold. Now imagine this mother has (n) kids and they are all very picky eaters, especially when it comes to fruit. So you cut the fruit up to specific sizes based on the preferences of the kids (context or size of the document chunked to the right size). Then you put each cut up fruit into a bowl based on what each of your (n) kids like (this is like embedding it giving it the numerical representation, or in this case putting it in a bowl). Finally you make (n) number of square jello molds for each kid so you can be sure none of the other fruit snuck into the other space. Finally you put all of the (n) jello molds together into a big cube based on the similarities of all the preferences. That way any kid allergic to strawberries can be sure their jello mold didnt come even close to a strawberry. (this is making the vector data base. Now when a kid asks for some dessert you wont have to search around for an area with their prefered fruit, you can be able to narrow the search quickly and find their piece or even a piece that isnt theirs specifically but is "close enough" in relation to their preferences. </p>

