I did a first read-through, and I could more or less parse it until Equation [3] in page 2. Around this point I lost track of notation, and I would need to ask some questions to understand what's really going on here. I assume the Appendix and the proofs are the parts you would like the most feedback on (as the other parts aren't really my area of expertise), but to be able to parse the statements of the theorems you cite there, I will probably need a bit more information. So if we could meet sometime, that would be good. 

In the meanwhile, let me attempt to outline some concerns I had up until the part I could parse, mainly so that I don't forget them in case we decide to discuss them in person. I will more or less attempt to order them in order of importance. 

*** There is a way to interpret Axiom 4 in a way that it contradicts Axiom 1. Axiom 1 implies the existence of some distance function between memories M_t and M_t+1, and the axiom is that the value of new information is simply a function of this distance between these sequential memory slots. Axiom 4, on the other hand, there is some other parameter, namely, "specificity", which is independent of the prior notion of "distance". It is assumed that if M_t changes to a M_t+1 in a way the "specificity" parameter is more, even if the changing distance kept fixed, E will increase more. (I assume by monotonic, you meant to say monotonic increasing.) 

I'm not sure if the concern here is clear, so let me try to explain it more concretely. Let's say E is just calories burnt, and M_t is our coordinates at time t. Axiom 1 says that E(t+1) only depends on |M_t+1 - M_t| (the distance). Axiom 4 says: "But also, the direction in which you travel is ALSO important. So if you travel the same distance uphill, you will burn more calories." Of course, this is not consistent.

*** This M^N notation does not make sense to me. If M^N is a number (as it denotes a maximum size), then what is S^T? From context, it is supposed to be a set. So I don't understand that paragraph very well, which might make my next concern possibly redundant. 

*** Why is this encoder f invertible? Are you claiming that this is invertible, or assuming that it is invertible? Either way, being invertible seems like a property which is critical enough to warrant some explaining. The "fact" that this encoder is invertible means that there is no way to do an action from to distinct memories, and arrive at the same memory. Perhaps this is a reasonable assumption, but perhaps not. For example, if the action was to commit suicide, I would assume the new memory would be the empty set, regardless of the original memory one starts with (I'm not being very serious here..) 

*** These next ones are purely notational that prevent me from understanding what's going on in Page 2. 

           - I don't understand the transition from a and a_t, or similarly s to s_t, or the "conditional expectation" in Equation 4, which says s=s_t
           - The paragraph which starts like "To write down the Bellman solution..." The end of that sentence seems like a grammatical error. The "for all" symbol is meant to quantify over a certain set, and then say something about those elements. Probably, what you want to say is \pi is a function s -> a, where s \in S and a\in A. The way a mathematician would write this is just \pi : S -> A, which is notation that means \pi is a function from the set S to the set A. 
           -  Some actual English grammar typos: "For example, in reinforcement learning exploration and exploitation both attempt to maximizes..."
                                                                          (There was one more error of the exact same type which I cannot see anymore, probably as my                                                                                  brain auto-corrects)


And finally I don't quite understand how this framework presents a way to tractably maximize both exploration and exploitation. Since this is probably explained in parts I don't quite understand yet, also this is by no means my area of expertise, I have not listed this as a concern, but it seems important that I understand this, so I wanted to ask about it. 

Somehow, the question of whether an agent should explore or exploit given the circumstances is algorithmically intractable (I'm not sure what this is supposed to formally mean) in the way the problem is traditionally formalized (I don't know what the tradition is) and by re-formalizing the problem, where the main difference is supposed to be exploiting and exploration are independent processes competing for time (I don't see how this is any different in essence from the classical exploration-exploitation dilemma), you are rendering the problem algorithmically tractable, because now it yields to dynamic programming.

To me, dynamic programming is a way of is just a way of not redoing computations that you have already done, so you just write them down somewhere in case you need to look them up later. If at each step of the process, if you only need to remember polynomially many things, and do only polynomially many stuff with them, then you can have a polynomial time algorithm. It is not clear to me how before the problem was not amenable to this type of analysis, and why it became so with the change in perspective you provided. 

Best,
Alp