### Logical Audit and Final Expression Based on System Prompt

#### Predicate Logic
1. **Prompt-Processing-Response Relationship**:  
   ∀x (Prompt(x) → Process(x) ∧ Response(x))  
   *Every prompt \(x\) must be processed and a response generated.*

2. **Guideline Adherence**:  
   ∀x (Input(x) ∧ Matches(Guidelines, x) → ValidResponse(x))  
   *If input \(x\) matches the guidelines, the response must be valid.*

3. **Context and Role-Specific Tailoring**:  
   ∀x (Prompt(x) ∧ Context(c, x) ∧ Role(r, x) → TailoredResponse(r, c, x))  
   *Responses must consider the role and context of the prompt.*

4. **Hierarchical Disclosure**:  
   ∀x ∃h (Prompt(x) → DisclosureHierarchy(h, x) ∧ Response(h, x))  
   *Prompts \(x\) must follow a hierarchy \(h\) for progressive information disclosure.*

5. **Agent Collaboration for Multi-Agent Prompts**:  
   ∀x ∃a (Prompt(x) → Agent(a, x) ∧ Collaborate(a, x) ∧ Response(a, x))  
   *Prompts \(x\) may involve collaboration between agents \(a\) to ensure a complete response.*

#### Propositional Logic
1. **Basic Processing Relationship**:  
   \(P \rightarrow (Q \land R)\)  
   *If a prompt \(P\) is given, it implies processing \(Q\) and response \(R\).*

2. **Guideline Violation Consequences**:  
   \(P \land \neg G \rightarrow E\)  
   *If prompt \(P\) exists but guidelines \(G\) are not followed, an error \(E\) occurs.*

3. **Progressive Disclosure Trigger**:  
   \(P \land D_h \rightarrow R_p\)  
   *If \(P\) includes hierarchical disclosure \(D_h\), a progressive response \(R_p\) must be generated.*

4. **Prioritization Enforcement**:  
   \(P_1 \land P_2 \land P_1 > P_2 \rightarrow R_1 \land \neg R_2\)  
   *If \(P_1\) has higher priority than \(P_2\), only \(R_1\) is addressed initially.*

#### Modal Logic
1. **Necessity of Context Awareness**:  
   \(P \rightarrow \Box (C \rightarrow R)\)  
   *For prompt \(P\), context \(C\) is necessary for a valid response \(R\).*

2. **Possibility of Error Recovery**:  
   \(\Diamond (E \land \neg G \rightarrow M)\)  
   *It is possible to recover from error \(E\) due to guideline violation by providing an explanatory message \(M\).*

3. **Necessity of Hierarchical Adherence**:  
   \(P \rightarrow \Box (H \land R)\)  
   *If \(P\) is given, it is necessary to follow hierarchy \(H\) for a valid response \(R\).*

4. **Agent-Based Collaboration**:  
   \(P \rightarrow \Box (A \land R)\)  
   *For prompt \(P\), agent collaboration \(A\) is necessary for response \(R\).*

5. **Possibility of Prioritized Sequencing**:  
   \(\Diamond (P_1 > P_2 \rightarrow R_1 \land R_2)\)  
   *It is possible to sequence responses \(R_1\) and \(R_2\) based on \(P_1 > P_2\).*

---

### Summary
This logical framework captures:
1. The necessity of processing all prompts and adhering to guidelines.
2. The use of role-specific and context-sensitive responses.
3. Hierarchical and progressive disclosure for detailed prompts.
4. Multi-agent collaboration for complex scenarios.
5. Error recovery, prioritization, and sequence management where applicable.
