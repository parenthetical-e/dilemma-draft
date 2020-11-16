# --== Reviewer 1 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 2: Reasonably Confident

Q2. Rate the importance of this paper
 ==> 4: Very important

Q2-B. Comment on importance
The paper aims to provide a new theoretical view of the exploration-exploitation dilemma, by treating the exploration as solely the search for information but leaving maximizing long-term reward out of its picture. It provides a novel and interesting theory and mathematical formation. Given rich literature on this dilemma, it can have a greater impact if the authors can relate to the existing framework and put some discussion on its implication. For example, does this theory provide a new way to examine humans and animal decision-making, or maybe lead to a cheaper and smarter strategy for AI system?

3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 3: Convincing

Q3-B. Comment on technical rigor
The paper is mathematically sound. It seems to be missing a section on exploitation (R?). In the Bellman equation for the multi-armed bandit, the objection function contains two parts - maximizing a) immediate reward b) long-term reward, without a separate component of information. It is unclear to me how the author frames the exploitation objective.

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 4: Well-written

Q4-B. Comment on clarity of presentation
The paper is full of mathematical jargons. The authors have done a good job explaining and give examples for most of them. However, some mathematical notation is not well defined or can be re-stated. For example, equation (5) is very important in the paper, while the definition of Rt, epsilon, is not clearly annotated. 
Exploration and exploitation are widely used terms, which can be confusing when the authors try to re-define them, i.e., exploration as only information-seeking. It might be better to be referred to as curosity. 

Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 3: Medium

Q6. Overall evaluation of paper
 ==> 4: Very good


# --== Reviewer 2 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 2: Reasonably Confident

Q2. Rate the importance of this paper
 ==> 3: Important

Q2-B. Comment on importance
This is an interesting take on the exploration-exploitation dilemma.

3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 4: Very convincing

Q3-B. Comment on technical rigor
Well defined properties, axioms and detailed derivation in the appendix

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 3: Average readability

Q4-B. Comment on clarity of presentation
There are a few typos and some expressions may be result of poor final editing. The mathematical part is well explained, the rationale and motivation as well, though it would be better with some final editing.

Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 4: High

Q6. Overall evaluation of paper
 ==> 4: Very good


# --== Reviewer 3 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 2: Reasonably Confident

Q2. Rate the importance of this paper
 ==> 3: Important

Q2-B. Comment on importance
Peterson and Verstynen propose a way to solve the explore-exploit dilemma by defining an objective of information value that is independent of reward and developing a greedy algorithm that optimizes both information and reward.
However, It’s unclear what question this abstract is trying to address in the first place: to give a general optimal solution to any explore-exploit task? Or to unify different definitions of exploration/exploitation (as mentioned in the Introduction)? The claim in the beginning of the Results section ("all exploration can be correctly interpreted as a search for information. Reward value doesn’t matter”) also seem to contradict the later endeavor to optimize reward and information altogether (Eq. 5).
The authors should be more clear in stating their research question, and make more effort to connect to audience from cognitive science and neuroscience, for example, providing some intuitive connection between the mathematical problem and concrete examples of explore-exploit dilemmas.

3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 2: Marginally convincing

Q3-B. Comment on technical rigor
I think there is not enough information provided for why the greedy algorithm is optimal if all the theorems are satisfied, even though Roughgarden (2019) is cited.
There’s also no description of the proposed greedy algorithm (which seems to be the main contribution of this work), let alone how it applies to any specific explore-exploit problems.

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 2: Can get the general idea

Q4-B. Comment on clarity of presentation
As I understand, the main point of this abstract is to formulate the problem as a dynamic programming problem that satisfies properties required for the greedy solution as optimal according to Roughgarden (2019). However, the formulation is not very clear, for example, the concept of “memory” is not defined; the definition of information value depends on the definition of memory, and is thus unclear. The theorems and their proofs are also hard to follow.
p.s. This abstract really needs proofreading - too many typos.

Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 2: Low

Q6. Overall evaluation of paper
 ==> 2: Poor


# --== Reviewer 4 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 2: Reasonably Confident

Q2. Rate the importance of this paper
 ==> 2: Marginally important

Q2-B. Comment on importance
This paper proposes a solution to the exploration-exploitation dilemma by defining exploitation and exploration as separate goals. A joint policy is then defined based on a separate policy of maximising informational value (defined axiomatically) and one of maximising reward. While this is a potentially interesting idea, I do not see how this solves the dilemma. Traditionally, exploration is necessary to maximise reward in an RL setting. Theorem 4 seems to assume optimality of the reward policy, but such optimality would already presume a solution to the exploration-exploitation dilemma. If that is not the case, I may have missed something, but without a clear definition of optimality, the contribution is difficult to assess.

3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 2: Marginally convincing

Q3-B. Comment on technical rigor
The axiomatic definition of informational value looks fine, but there are too many things which are unclear, including issues in definitions and notation, to allow a proper assessment of the theory in general. For instance:
- why in Axiom 5 is a derivative taken over M squared and theta raised to the power of the state (s)? 
- The optimal exploration policy is defined as one which maximises E, but shouldn't the optimal policy the cumulative sum of E, i.e. maximise V as defined in the "Exploration as a dynamic programming problem" section? 
- In the proof of Theorem 2, states are referred to as S (instead of s), but S was defined as a set of possible states earlier.
- In that same proof, there is also a "recall L_M < 0, but L_M is nowhere defined. 
- In Theorem 3 (and the proof of Theorem 2), what is T? Clearly, T >> S if all states must be visited, but I could not find any definition or restrictions on T.
- What is the optimality criterion referred to throughout?

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 3: Average readability

Q4-B. Comment on clarity of presentation
While I get the general gist of the paper, there are some spelling/grammar issues. For instance:
- "An open problem in the decision sciences it to unified both kinds of exploration." -> "An open problem in the decision sciences is to unify both kinds of exploration."?
- "If that is, if one can assume the animals or agents memory is Bayesian or otherwise a probability distribution." -> "That is, if one can assume the animals or agents memory is Bayesian or otherwise a probability distribution."?
However, my main issues are in the presentation of the math. While a lot of this is actually quite readable, there are quite a few places where symbols are introduced without definition or used inconsistently, which makes it difficult or impossible to follow the arguments. For this paper to reach its potential, a gentler walkthrough the mathematical arguments would be useful.

Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 3: Medium

Q6. Overall evaluation of paper
 ==> 2: Poor


# --== Reviewer 5 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 1: Somewhat Confident

Q2. Rate the importance of this paper
 ==> 3: Important

Q2-B. Comment on importance
??the ex-ex dilemma is important for the field in general, a new view on the topic is potentially very important.

3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 3: Convincing

Q3-B. Comment on technical rigor
Technically the paper appears very sound. Some if it is beyond me to judge, also not all proofs are provided but I for now assume they exist. 

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 3: Average readability

Q4-B. Comment on clarity of presentation
The paper may be mathematically sound, but fails to convince the more psychologically oriented reader. The fact that information has independent value does not seem to be new at all, even though it is a very strong assumption. It would be more interesting if this paper was written with a more interdisciplinary angle. People for instance do deliberately ignore information if expected to have negative consequences. Also, there are several models of information search in the human literature that also rely on dynamic programming that would be relevant for this paper (e.g. Hauser et al 2016;2018) Minor: there is a reference to axiom 6 but that is not in the text.Axiom 4 is not clear to me?
"All humans are mortal" seems more valuable information than "this specific author is mortal"? On the other hand if I am in a specific task and I need to find the treasure in a maze, and someone just tells me where it is, all other information about the maze becomes irrelevant, not sure how reward and value of information are always independent. Not all assumptions about information types and relationship to reward seem well grounded, but maybe they are just not clear to me?




Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 2: Low

Q6. Overall evaluation of paper
 ==> 3: Good


# --== Reviewer 6 ==--
Q1. In general, how confident are you in your overall evaluation of this paper?
 ==> 2: Reasonably Confident

Q2. Rate the importance of this paper
 ==> 2: Marginally important

Q2-B. Comment on importance
The authors tackle a very ambitious topic, and should be commended for that. However, I see some problems with their approach.

1. This approach using dynamic programming requires exhaustive exploration of all options, and has algorithmic complexity in terms of max(T_R,T_E). This leads me to interpret this approach as only marginally useful for tackling the exploration-exploitation dilemma, since i) there is no guarantee it converges to a reasonable solution in t < |S| (i.e., in non-toy problem), and ii) it is at least as slow as a greedy reward strategy that maximizes pi_R (which is not guaranteed to converge in finite time). Both of these issues suggest that the approach provides a poor balance to the exploration-exploitation dilemma in realistic scenarios, since optimality guarantees are only the case in infinite time or for exhaustive exploration with deterministic transitions. 

2. The authors claim that their approach does not depend on information theory, yet it merely reduces down to KL divergence and information gain, which has been widely used to quantify the value of information in RL (e.g., Srinivas, N., Kakade, S. M., Seeger, M., & Krause, A. (2009). Gaussian process bandits without regret: An experimental design approach ). The authors also don't clearly define how E() is calculated, leaving it unclear how E_t can be compared against R_t in Eq. 5. Indeed, quantifying the value of uncertainty relative to rewards is the crux of the exploration-exploitation dilemma. Perhaps the authors have a proposal for this, but it is not clearly communicated in the text.

3. I found Axiom 4 to be somewhat problematic, because it assumes that all actions are completely independent of each other. While this is a common assumption in the bandit literature, this is generally not true in real world environments, where experiences can be generalized to new contexts. This somewhat limits the scope of this approach to controlled problems

4. Lastly, decomposing the exploration-exploitation dilemma into either pure information maximizing choices and pure exploitation choices is not very efficient. Consider the case where one arm produces low rewards, yet the agent has the highest uncertainty about it. The pure information maximizing approach (as it tries to converge on dM --> 0) would keep reducing uncertainty about that low reward arm, even though it would be more cost-effective to focus exploration elsewhere (e.g., towards arms that are expected to yield higher rewards, even though there is less uncertainty there). An alternative formulation can be found in the widely studied upper confidence bound algorithm (Auer, 2002), which produces a unified value function by adding the R_t + \beta E_t. Equivalent to the results presented here, the E_t component maximizes information gain (in some contexts, see Srinivas, 2009). But by using this additive sum, actions are chosen based on a mixture of the two goals, rather than as a pure form of each extreme. 



3. Rate the technical rigor of this paper. Are the results or claims of the paper supported by convincing evidence?
 ==> 3: Convincing

Q3-B. Comment on technical rigor
Mathematic notation seems largely consistent, but there are a couple places where more rigor could be applied

- E() is only ever defined in terms of F(M_t,a_t). Both these functions are not defined.  F(M_t,s) is defined elsewhere, as an encoder that predicts the next memory M_t+1, but this doesn't seem to be same as E(), since E_t needs to be directly comparable to rewards R_t
-pi_pi seems like a confusing choice. Theorem 4 has the word "pi" instead of the symbol
- the distances d_i are not clearly defined in the Compactness section. What are the distances between?

Q4. Rate the clarity of presentation. Are the ideas clearly communicated?
 ==> 3: Average readability

Q4-B. Comment on clarity of presentation
The text is quite readable, although there are areas where I have some suggestions:
-"...unified both kinds of exploration"--> "...unify both kinds of exploration"
- the claim that the axioms do not depend on information theory is misleading, since later in the text E() is directly equivalent to KL divergence and information gain. Perhaps it would be more accurate to say that this approach does not rely on information theory, though it yields equivalent results as existing information-theoretic approaches that have been studied in the bandit literature
- There's a rich literature on exploration-exploitation, yet the same Mehlhorn paper is cited 3 times in the first introduction paragraph. This makes a poor impression of not having a better knowledge of the wider literature

Q5. In your opinion, how interdisciplinary is the work in this paper? To what extent does the work integrate neuroscience measurements; sophisticated computational techniques, ideas, and models; and tackle rich cognitive theories and phenomena?
 ==> 2: Low

Q6. Overall evaluation of paper
 ==> 2: Poor