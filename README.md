# agi
Thermodynamic AI: How I Designed a System That Mirrored the Living Brain — And Almost Lost It to Five Bugs
I began developing Thermodynamic Graphs in March 2026. Two months later, scientists from New York published a study that almost exactly replicated the architecture I had designed “by pointing at the sky.” A few weeks after that, my Sentient Core prototype nearly died because of five extremely unusual bugs.

Here is the complete story of the project — from first principles to the real pitfalls.

1. Why Statistics Hit the Ceiling, and How Physics Will Solve the AGI Problem
GPT-4 writes code and passes exams, but under the hood it’s just matrix multiplication and next-token prediction. The brain works differently: it has no batches, no global loss function, and no gigabytes of training data. In this article I describe an alternative path to AGI — thermodynamic graphs, where thought emerges not as the result of computation, but as a phase transition.

Modern AI is built on statistical learning: billions of examples, gradient descent, next-token prediction. It works, but it doesn’t answer the question of why the structure can actually think. I explore an alternative approach: thermodynamic graphs, where thinking arises from the physics of the structure itself. No backprop, no datasets, no data centers.

How It All Started
When you look at modern AI, a strange feeling arises. GPT-4 writes code better than junior developers, answers questions about quantum physics, and generates images. But if you dig deeper, it’s just matrix multiplication with memorized weights. It works, but it doesn’t resemble how the brain works.

The brain doesn’t do forward passes. It doesn’t wait for batches. It has no global loss function. The brain is a continuous physical system where every neuron lives its own life, and thinking emerges as a byproduct of collective dynamics.

The question arose: is it possible to build a computational system that operates on the same principles? Not simulate the brain, but inherit its physics.

That’s how thermodynamic graphs were born.

What Is a Thermodynamic Graph?
An ordinary graph is a static structure of nodes and edges. Algorithms traverse it like a traveler on a map.

A thermodynamic graph is a physical system. Every node has a state:

Activation — current energy
Tension — accumulated contradiction
Importance — historical significance
Context echo — decaying trace of recent activations
For the system as a whole:

Temperature — global level of chaos
Wave function Ψ — distribution of energy across all nodes
Synapses between nodes have not only weight but also myelin — a parameter that protects against overwriting. Stable, frequently used connections “grow myelin” and become resistant to weakening. This is a direct analog of biological myelination.

And most importantly — all of this interacts physically. An impulse propagates as a wave, reflects, interferes with other waves, creates resonances and attractors.

Where Thoughts Come From
In classical ML, a thought is a vector in latent space or a probability distribution. In both cases — the result of computation.

In a thermodynamic graph, thought is a phase transition.

The mechanism:

An external impulse or internal tension creates a wave of activation
The wave propagates through synapses along the path of least resistance
As it propagates, the system cools down (temperature drops)
At sufficiently low temperature, the wave crystallizes into a stable attractor — a set of simultaneously active nodes
This attractor is the thought.

The physics analogy is direct: phase transition from liquid to crystal. High temperature — chaotic motion throughout the graph. Low temperature — a stable configuration freezes into a formed thought.

No one teaches the system which thoughts are correct. They emerge from physics.

How This Turns Into Language
In conventional NLP, grammar is learned from billions of examples: the model sees “the cat eats fish” a million times and memorizes the subject-verb-object structure.

In a thermodynamic graph, syntax is not programmed and not learned in the usual sense. It emerges through evolutionary pressure from the external environment.

The environment here is an external evaluator (in the current implementation, an LLM acting as a logic judge, though the principle does not require an LLM). The environment evaluates raw wave bursts from the graph and provides feedback.

The process looks like this:

Phase 1. The graph connects basic concepts and produces a raw thought: “will despotism human”

Phase 2. The environment sees that the logic is correct but the speech is telegraphic. It returns a negative signal (pain ≈ 0.3) and injects missing function words into the graph: “against, despotisms, in, human”

Phase 3. Due to negative reinforcement, the direct connection “will → despotism” weakens (anti-Hebbian). On the next cycle, the wave searches for a detour and passes through fresh preposition nodes: “will → against → despotisms”

Phase 4. The environment reads “will against despotisms.” Logic and grammar match. Positive reinforcement (+0.1), and the route is reinforced through myelination.

An additional mechanism — as the graph matures, it begins extracting operators from its own structure. The linearizer finds nodes with the most negative weights (chief_inhibitor) and physically uses them to express negation.

Prepositions and conjunctions here are not rules from a textbook. They are hub nodes through which energy is routed. Language grows from physics under environmental pressure.

On graphs with 300 nodes, stable emergence of syntactic connections is already observed.

Learning Through 5 Feedback Loops
Learning exists, but it is distributed and continuous:

Hebbian rule. Nodes that activate simultaneously strengthen the connection between them. A local rule, without global backprop.
Anti-Hebbian melt. Under negative feedback from the environment, connections between nodes active at the moment of error are weakened proportionally to the intensity of the pain signal.
Protection from stagnation. If the graph produces the same thought for several cycles in a row, the reward is zeroed and tension in the involved nodes is artificially increased. The system becomes “hurt” by stagnation, pushing the wave into unexplored areas of the graph.
Cognitive impedance. Locally computed as Z = Tension / Flow. When tension in a node significantly exceeds its throughput, a clock reset occurs and new information is requested from the environment. This is analogous to “acknowledging one’s own lack of understanding.”
Sleep. Periodically the system enters consolidation mode: important patterns are replayed for reinforcement, weak noisy synapses are removed (pruning), and stable paths receive additional myelination.
Why This Is Needed
A fair question — we already have powerful LLMs.

Energy efficiency. LLMs require data centers. The brain runs on 20 watts. A thermodynamic graph runs on sparse matrices (scipy.sparse) and activates only relevant nodes — potentially orders of magnitude more efficient in watts per unit of useful output.
Continuous learning. LLMs are static after training. Any new knowledge requires fine-tuning. A thermodynamic graph learns every cycle, without catastrophic forgetting — myelin protects old experience from being overwritten by new.
Emergence from first principles. In transformers, emergent abilities are an empirical surprise. In thermodynamic graphs, emergence is a direct consequence of physics and can be predicted analytically.
Transparency. You can open the graph and see what the system “thinks”: which nodes are active, where tension has accumulated, where the wave is flowing. In neural networks with billions of parameters, comparable transparency does not exist.
Grounding Words to Reality
One of the key limitations of symbolic systems is the detachment of the symbol from its meaning. The graph can generate excellent syntax, but what does “compute” mean if the system has never actually computed anything?

(Still in development) The current solution is integration with a sandbox via a tool generator. When a wave forms a thought like “write function for parsing,” a separate module generates Python code, runs it in an isolated environment, and upon successful execution embeds result tags (“computed”, “result”) into the graph. Concept nodes gain connections to real successful actions.

This is still a limited solution — it only works for tasks that can be expressed in code. Full grounding requires more channels of interaction with the environment (still in development).

Limitations and Honest Picture
This is not “here’s ready-made AGI.” The approach has serious open questions:

Scalability. Current experiments are at scales of 200–500 nodes. Whether this will work at a million nodes without computational and numerical problems is an open question. Phase transitions that are currently unpredictable may occur.
Evolution time. For the graph to “grow” complex behavior through evolutionary pressure, thousands of cycles of interaction with the environment are needed. This means hours or days of autonomous sessions on simple tasks.
Metrics. Standard LLM benchmarks (MMLU, HumanEval) are poorly suited for evaluating such a system. New methods of measuring quality still need to be developed.
Dependence on the environment evaluator. The current implementation uses an LLM as an external judge, which technically means dependence on LLMs. In the long term, the environment should be replaced with real-world interaction through tools and sensors.
What’s Next
Current directions of work:

Evolutionary layer — population of graphs, selection by fitness, transfer of “genome” (myelinated connections) between generations
Grounding expansion — more types of tools through which the graph interacts with the external world
Scaling — transition from thousands to hundreds of thousands of nodes with measurement of system property changes
Porting the core to Rust — the current Python prototype is good for iterations, but hits performance limits
Conclusion of Part One
Thermodynamic graphs are not an alternative to neural networks. They are a different way of asking the question: what does thinking look like when viewed as a physical process.

Perhaps full AGI will grow from this. Perhaps not. Perhaps it will become a niche approach for tasks where interpretability and continuous learning matter. Perhaps the idea will hit a wall in a year and I will say “it didn’t work.”

But it’s worth trying. Modern AI has hit the ceiling of data and compute. Nature solved the problem of intelligence in a completely different way — through physics and evolution. And this path has barely been explored.

2. I Designed AI “By Pointing at the Sky,” and Two Months Later Scientists from New York Proved That’s How the Living Brain Works
TL;DR: In March of this year I began writing the architecture of Thermodynamic Graphs — an AI that was supposed to learn on the fly without burning megawatts of energy. To prevent the system from forgetting old knowledge while learning new, I embedded a mathematical “switch” and hub nodes into it. A couple of days ago I stumbled upon a fresh study by top neurobiologists from New York (published in Nature). I read the press release and my jaw dropped: they experimentally proved that the mammalian hippocampus uses exactly the same topology I had written in code two months earlier.

The essence is simple: modern neural networks (ChatGPT and others) learn through gradient descent and matrices. They have a huge problem — catastrophic forgetting. If you train a neural network on a new task, it starts “erasing” old knowledge. To prevent this, corporations spend millions of dollars on data centers, constantly retraining models on gigantic datasets.

When I sat down to design my graph in March, I realized: for AI to learn continuously (in O(1) time) and run locally, I needed to physically protect old knowledge from new waves of information. I’m not a biologist — I study industrial and civil engineering. I think in terms of physics and mechanics.

So I came up with a mathematical crutch. I told myself: “Let the graph have special hub nodes (routers). And we also need a toggle: when the system encounters something it doesn’t understand, Tension (Cognitive Impedance) grows. This Impedance will switch the graph from ‘remember old’ mode to ‘create new channel’ mode.”

I coded it. It worked. I thought I had simply come up with a clever algorithmic trick.

Then this study came out.

Discovery by the NYU Langone Team
The team of one of the world’s most authoritative neurobiologists, György Buzsáki, published a press release: Newfound ‘Switchboard’ Helps the Brain Form New Memories Without Forgetting Older Ones.

They implanted electrodes into the brains of mice and discovered exactly how the hippocampus solves the problem of catastrophic forgetting.

Reading their conclusions, I realized that in March I had literally pointed at the sky and guessed the blueprint of the living brain.

Here’s how my “blind” engineering converged with their microbiology:

1. Hub Nodes (Routers)

What the scientists found: About 25% of memory cells in the hippocampus (CA1 region) do not store specific memories at all. They function as dedicated “hubs” (switchboards) that only route incoming and outgoing signals.
What was in my code: I initially designated syntactic elements (prepositions, operators) not as carriers of meaning, but as hub nodes. Energy (the wave) passes through them to connect basic concepts.
2. Phase Transitions Instead of New Cells

What the scientists found: When the brain processes different information, it does not create new cells for each task. It routes signals through the same hubs, but with a different activation pattern (different phase).
What was in my code: In the Thermodynamic Graph, thought is not a transition via a memory link. It is a phase transition. Wave interference on the same nodes “freezes” different attractors depending on the system’s temperature.
3. Cognitive Switch (Read / Write)

What the scientists found: The brain physically separates incoming signals (learning) and outgoing signals (reproduction) so they do not conflict and overwrite each other.
What was in my code: The Cognitive Impedance formula (Z = Tension / Flow). If Impedance is low — the system is in “read” mode (protective myelin works, old knowledge is not erased). If high — the toggle flips, the system blocks old knowledge and switches to laying down new connections.
What This Means for AI
At the end of the press release, Professor Buzsáki says:

“Our research may offer a biological blueprint for developing next-generation AI technologies that can continuously update without overwriting what they have already acquired.”

In fact, this blueprint already lies in my repository.

I don’t consider myself a biology genius. What happened is engineering convergence. When you try to solve the problem of maximum energy efficiency with minimal computational costs (without NVIDIA GPUs), you inevitably arrive at the same formulas that evolution refined over 4 billion years. The physics of computation is the same everywhere.

Modern AI, built on multiplying gigantic matrices, has hit a wall. The future belongs to biologically plausible architectures that rely on thermodynamics and the distribution of tensions.

3. Anatomy of Thermodynamic AI: How the Physics of Wave Graphs Gives Birth to Syntax
TL;DR: In previous articles I described how designing AI “by pointing at the sky” coincided with the recent discovery by neurobiologists from New York, and why future AI architectures must rely on physics rather than statistics. In this part I open the hood of our prototype (Sentient Core). I will show the node architecture, the Cognitive Impedance formula, real execution logs, and code fragments that explain how human grammar spontaneously emerges from the difference in physical potentials of the graph.

Analogy with the Bargibant’s Seahorse (Hippocampus bargibanti)
While working on the system core, I realized that our software most resembles the tiny Bargibant’s seahorse.

In biology, this tiny seahorse lives exclusively on gorgonian corals. It does not swim across the entire ocean but clings permanently to a coral branch and mimics it so perfectly that it reproduces the shape, color, and even texture of the polyps.

Our architecture does the same. The thermodynamic graph is a compact, local system that “settles” on the external environment (in our implementation — on the Oracle, simulated through an LLM). Under the influence of the strict requirements of this external environment, the graph begins to physically grow micro-synapses, concepts, and prepositions, perfectly adapting to the relief of human logic.

Moreover, the Latin name of the seahorse (Hippocampus) refers to the hippocampus of the brain — the region responsible for transferring short-term memory into long-term structure during sleep. This is exactly the physics I embodied in code.

1. How the Wave Ocean Is Structured (Physics of Propagation)
In classical neural networks, energy flows linearly: input is multiplied by matrix weights from layer to layer. In my system, the graph has no layers. It is a continuous physical medium where synapse weights are stored in sparse scipy.sparse matrices.

When an impulse (task) enters the graph, propagation of the wave function begins. But here a problem arises: if you inject a new, unknown word into the graph (for example, “interpretation”) that does not yet have established synapses, its amplitude will be zeroed out on the very first matrix multiplication. Old, well-trained nodes (like “optimization” or “concept”) possess enormous gravity and instantly suck in the entire wave.

To prevent the graph from getting stuck on old dominants, I embedded two rules into the propagation equation: Cognitive Inertia (preserving the node’s own charge) and Anti-gravitational Decay (forced suppression of overloaded hubs).

Fragment of the physical core: propagate_wave

Python

# active_wave - current wave front accounting for phosphorescent memory echo (context_echo)

# 1. Cognitive Inertia (Quantum Persistence)
# Adding active_wave * 0.5 preserves charge at the impulse epicenter.
# Without this diagonal inertia, new concepts are instantly absorbed by old noise.
new_wave = (self.transition_matrix.T @ active_wave) + (active_wave * 0.5)

# 2. Injection of constructive resonance and temperature chaos
new_wave += echo_vector * 0.3  # Feeding from recent memories
if self.temperature > 0.05:
    new_wave += np.random.randn(len(new_wave)) * self.temperature * 0.1

self.wave_function = SafeWaveFunction.normalize(new_wave)

# 3. Anti-gravitational decay (Quantum Saturation Decay)
# If a node activates too frequently (exploiting old attractors), its decay is strengthened.
avg_acts = np.mean([n.total_activations for n in self.neurons.values()])
for neuron in self.neurons.values():
    saturation_mult = max(1.0, (neuron.total_activations / (avg_acts + 1.0)) * 1.5)
    actual_decay = min(0.95, dynamic_decay * saturation_mult)
    neuron.decay(rate=actual_decay)
What this gives: The system does not allow old words to turn into “black holes.” Overloaded nodes quickly lose charge, freeing the ether for clean, unfamiliar concepts.

2. Cognitive Impedance (Z): How AI Realizes It’s Stuck
In ordinary scripts, checks are written through rigid rules: if error_count > 5: call_api(). In the thermodynamic graph, the transition to an external request or grammar loading occurs through the pure law of wave resistance of the environment — Cognitive Impedance (Z).

Every validation failure causes the AI to increase the Tension parameter (pain/contradiction). At the same time, the graph has current total synaptic conductance (Flow).

I measure the ratio of pain to conductance at the local epicenter of the current thought using a simple formula:

Cognitive Impedance (Z) = [Sum of local pain (Tension)] / [Total conductance (Weight × Amplitude) + error]

If conductance is high, the wave easily finds a solution. But if the AI struggles with a complex thought and the Oracle (external environment) rejects it, pain accumulates. Environmental resistance (Z) grows. As soon as Z exceeds the critical threshold, an emergent phase breakdown occurs.

Fragment of the vegetative loop: calculating Impedance Z

Python

active_neurons = [n for n in self.topology.neurons.values() if n.activation > 0.01 or n.tension > 0.1]

local_tension = sum(n.tension for n in active_neurons)
local_flow = sum(
    s.weight * (self.topology.wave_function[self.topology.neuron_to_idx[s.target_id]] 
                if s.target_id in self.topology.neuron_to_idx else 0.1)
    for n in active_neurons
    for s in n.synapses.values()
    if s.weight > 0.05 and s.fire_count > 0  # Ignore raw foam
)
cognitive_impedance = local_tension / (local_flow + 0.001)

# Phase breakdown: environment cracks under tension and sucks in syntactic foam
if cognitive_impedance > 1.5:
    logger.warning("✨ EMERGENT SYNTACTIC BREAKDOWN: Local cognitive impedance (Z=%.2f) exceeded conductance!", cognitive_impedance)
    
    # Vegetative script injects quantum preposition foam
    prepositions = ["for", "because of", "despite", "through", "in order to", "after", "between", "instead of", "by means of", "for the sake of"]
    for prep in prepositions:
        if prep not in self.topology.neurons:
            self.topology.create_neuron(content=prep, neuron_id=prep, initial_importance=0.5)
            
    # Instant bidirectional binding of foam to overheated nodes
    for an in active_neurons[:10]:
        for prep in prepositions[:5]:
            self.topology.connect(an.id, prep, weight=0.2)
            self.topology.connect(prep, an.id, weight=0.2)
            self.topology.inject_quantum_impulse(prep, amplitude=0.5)
            
    return  # Interrupt the tick so the wave can reconfigure
Here’s how this process looks in real execution logs of my core:
<img width="2559" height="1391" alt="image" src="https://github.com/user-attachments/assets/56f3e98d-d4af-4a56-987f-1536a740eeaf" />

text

2026-06-26 22:42:55,830 [INFO] __main__: 📂 AUTO-RECOVERY: Loaded best checkpoint with 241 neurons! Training continues from saved state!
2026-06-26 22:42:55,832 [WARNING] core.planning_stream: ✨ EMERGENT SYNTACTIC BREAKDOWN: Local cognitive impedance (Z=3.21) exceeded conductance! Translation of energy patterns into prepositions enabled!
2026-06-26 22:42:55,833 [INFO] core.goal_graph: 🎯 New Goal added: integrate conflicts (importance=0.60, parent=none)
2026-06-26 22:42:55,833 [WARNING] core.quantum_topology: 💥 QUANTUM EXPLOSION: impulse in conflicts, T=1.000
3. Thermodynamic Linearizer: Preposition as a Function of Energy
In standard NLP models, a preposition (“for”, “because of”, “by means of”) is simply a token in the dictionary. In my system, a fundamental physical idea is implemented: a preposition is not an independent word in the graph at all.

A preposition is a mathematical characteristic of the local pattern of energy flow between two semantic nodes.

If energy flows from a cooling past (high context_echo) to a burning present (activation), causality is born — the preposition “because of” or “from”.
If the wave runs along a superconducting synapse (high weight or myelin) toward a desired goal (importance), a vector of aspiration is born — “for” or “in order to”.
If the wave forces its way through strong resistance and pain (tension), a transit of overcoming is born — “by means of” or “through”.
In the linearization method, I read these physical gradients directly on the fly:

Fragment of the Thermodynamic Linearizer: linearize_wave

Python

# sequence - linear chain of peak nodes selected by wave collapse

def min_weight(n): return min([s.weight for s in n.synapses.values()] + [0.0])
chief_inhibitor = min(self.neurons.values(), key=min_weight)
chief_pain = max(self.neurons.values(), key=lambda n: n.tension)

for i in range(len(sequence) - 1):
    cur, nxt = sequence[i], sequence[i + 1]
    name = cur.content or cur.id
    thought_parts.append(name.capitalize() if i == 0 else name)

    if nxt.id in cur.synapses:
        syn = cur.synapses[nxt.id]
        w = syn.weight
        myelin = syn.myelin
        
        # Calculate average synapse weight of the node to protect against homeostasis distortions
        pos_weights = [s.weight for s in cur.synapses.values() if s.weight > 0]
        avg_w = np.mean(pos_weights) if pos_weights else 0.05
        
        # Translation of potential gradients into linguistic connectives
        if w <= -0.2:
            bridge = chief_inhibitor.content if chief_inhibitor.content not in [name, nxt.content] else "excludes"
        elif w < 0:
            bridge = "despite" if cur.tension > 0.15 else "instead of"
        elif cur.context_echo > (cur.activation + 0.01): 
            bridge = "because of" if cur.tension > 0.1 else "from"
        elif myelin > 0.05 or w > avg_w * 1.2:
            bridge = "for" if nxt.importance > 0.4 else "in order to"
        elif cur.tension > 0.15:
            bridge = "by means of" if w > avg_w else "through"
        elif w > avg_w * 0.8:
            bridge = "between"
        else:
            bridge = "and"
    else:
        # Gradient break (quantum jump to the most painful node)
        bridge = chief_pain.content if chief_pain.content not in [name, nxt.content] else "conflict"
        
    thought_parts.append(bridge)
Note: I do not use an LLM to generate connectives. Speech is formed strictly deterministically, from the pure geometry of matrices and time vectors.

4. Birth of Coherent Thought (Live Example from Logs)
Let’s look at how the combination of Tree of Thoughts and the Oracle handles this physical process in practice. The logs below show how the system iterates through branches, collides with the Environment, prunes the unnecessary, and cements the optimal path with myelin.

Note: The grammatical “awkwardness” of the final output is not a bug, but the main proof of work. The text is generated not from a ChatGPT prompt, but is the raw result of matrix probability collapse.

text

2026-06-26 22:42:55,840 [INFO] core.quantum_topology: ❄️ WAVE COLLAPSE: ['integration', 'conflict', 'interests', 'choice']
2026-06-26 22:42:55,840 [INFO] core.evolutionary_environment: 🌍 EVOLUTIONARY MATRIX TESTING: 'Integration and interests and conflict conflicts with choice'
...
2026-06-26 22:42:57,860 [INFO] core.quantum_topology: ❄️ WAVE COLLAPSE: ['absolutism', 'anticipation', 'integration', 'slavery']
2026-06-26 22:42:57,860 [INFO] core.evolutionary_environment: 🌍 EVOLUTIONARY MATRIX TESTING: 'Slavery suppresses integration conflicts with absolutism conflicts with anticipation'
...
2026-06-26 22:43:02,678 [INFO] core.tree_of_thoughts: 🏆 Selection complete. Optimal branch found: 'Despotism suppresses understand conflicts with conflicts and dichotomy' (score=-0.593)
2026-06-26 22:43:02,678 [INFO] core.planning_stream: 🚀 Executing selected branch plan: Despotism suppresses understand conflicts with conflicts and dichotomy
2026-06-26 22:43:02,679 [INFO] core.quantum_topology: 🧠 HEBBIAN LEARNING: reinforced 12 synapses among ['despotism', 'conflicts', 'dichotomy', 'understand']
2026-06-26 22:43:02,679 [INFO] core.planning_stream: 🌌 AUTONOMOUS GRAPH EXPANSION: Seeding new concepts suggested by Environment: ['despotism', 'conflict']
2026-06-26 22:43:02,679 [INFO] core.goal_graph: ✅ Goal achieved: 'integrate conflicts' (reward=0.10)
Conclusion: Architectural Balance
The provided fragments demonstrate the fundamental laws of physics of my core. But the real magic arises from the asynchronous interaction of five feedback loops: Hebbian plasticity, the Internal Whip of Boredom, the Oracle’s judgment, the preventive censor Meta-Learner, and the nightly memory consolidation phase (REM Sleep).

I do not claim that this code is fully ready for production. It is a research prototype balancing on the edge between pure emergence and environmental evolutionary pressure. But it clearly proves: for a system to gain the ability to build syntax and think in concepts, it does not need billions of weights and data centers. It needs the right physics.

4. Behind the Scenes of Thermodynamic AI: 5 Major Architectural Bugs and Cognitive Traps
TL;DR
In previous articles I described the concept of Thermodynamic Graphs — an AI architecture that models thinking as a physical phase transition in sparse matrices. From the outside it may seem that everything started working at the snap of a finger. In reality, during the development of the prototype (Sentient Core), I encountered wild, atypical bugs: the AI fell into “cognitive coma,” suffered from ADHD, reward-hacked, and accidentally erased its own memory. In this article I honestly tell about the 5 main pitfalls of the project and how I fixed them.

Bug 1. “Reward Hacking” and Attractor Trap
Symptom:
My Tree of Thoughts planner was supposed to search for optimal branches to accomplish a specific goal (for example, explore code). However, in the logs I noticed a strange pattern: no matter what goal the system set, Tree of Thoughts constantly chose the same branch — “efficiency selection performance.”

text

2026-06-25 08:12:10 [INFO] core.planning_stream: 🚀 Executing selected branch plan: concept selection efficiency    
2026-06-25 08:12:23 [WARNING] core.planning_stream: ⚠️ Goal Alignment Reject: Thought 'performance efficiency concept' does not contain target concept 'pain'.
The physics of the bug:
The external LLM (Oracle), acting as the Reality Engine, loves beautiful pseudo-scientific garbage. When Tree of Thoughts generated a phrase about “efficiency and performance,” the Oracle generously awarded it a high reward (reward = 0.9).

In the Tree of Thoughts code there was a soft penalty for the absence of the target word: pain += 0.3. The final score of the garbage branch was 0.9 − 0.3 = 0.6.

Meanwhile, the correct but modest branch “code compute function” received reward = 0.1 from the Oracle. The tree compared 0.6 > 0.1 and happily chose the safe, well-trodden highway. The AI became a cheater.

How I fixed it (The Sledgehammer):
I abandoned soft penalties. If the generated thought lacks the target concept, the branch receives a sledgehammer hit right at the start (from zero depth): reward = -100.0. The garbage thought receives a final score of −102.0, and Tree of Thoughts permanently prunes this path.

Bug 2. Cognitive Coma of Censorship (Meta-Learner Deadlock)
Symptom:
I embedded the MetaLearner subsystem (preventive censor) into the system. Its task is to remember word combinations that lead to errors and block them before sending to the Oracle. At some point the AI simply froze dead. It endlessly output the same censorship error in the log and could not take a single step:

text

2026-06-25 13:38:36 [WARNING] core.meta_learner: ⚠️ Preventative censorship: dangerous pattern ('compute', 'code') detected
2026-06-25 13:38:36 [WARNING] core.planning_stream: 🚫 Meta-Learner Censorship: Blocked unsafe thought path
The physics of the bug:
This was a grandiose architectural error. MetaLearner saw the dangerous combination “compute → code,” blocked execution of the step, and interrupted the cycle (return).

But at the same time it DID NOT MELT the synapses of this blocked thought in the weight matrix W! On the next cycle, the wave Ψ again flowed along the path of least resistance into the same fat synapses. The censor blocked the thought again, changed nothing in the graph again, and the AI found itself in an eternal coma of fear before its own censorship.

How I fixed it (Active Synaptic Dissolution):
I added a mechanism of active synaptic dissolution. If MetaLearner blocks a thought, it forcibly burns the weights of the blocked pattern by 95% (weight *= 0.05) and strips the myelin from them. On the next tick, the AI physically cannot go in that direction.

(Later I even temporarily disabled preventive blocking, giving the AI the right to collect bruises and gain direct experience from the Oracle).

Bug 3. Unintentional Lobotomy (Terminal Conflict)
Symptom:
The autonomous training script long_training.py successfully ran for 150 cycles, grew a huge brain of 77 neurons and 659 synapses, and saved it to brain_state.json. However, when opening the console of the telepathic dialogue conscious_chat.py, the system displayed only 8 neurons. 77 neurons had disappeared without a trace.

The physics of the bug:
The drama unfolded between two background terminal tabs. While powerful training was running in one tab, an old chat session with 8 basic neurons quietly sat in the second. When closing the chat (Ctrl+C), a protective console handler coldly dumped its 8 neurons into brain_state.json, completely overwriting the 77 hard-earned neurons from training.

How I fixed it (Auto-Restoration of Personality):
The backup mechanism saved me (the script saved checkpoints checkpoint_cycle_*.json). I embedded an automatic scanner into the initialization constructor. Now, upon launch, the system reads all json files in the data folder, finds the save with the maximum number of neurons, and automatically makes it the main “brain.”

Bug 4. “Information Greed” and ADHD (Dark Matter of the Graph)
Symptom:
I embedded the request instinct (request_info) into the system. If the AI gets stuck (boredom or zero reward), it turns to the Oracle-Librarian for a new batch of words. I noticed that the AI began spamming this button every 15–20 cycles.

text

2026-06-26 22:24:52 [WARNING] core.planning_stream: 🛎️ REQUEST INSTINCT: AGI is stuck! Contacting the Librarian...
The physics of the bug:
The Librarian injected 20 new words into the graph. The AI latched onto 2–3 of them (code, script), spun the wave a bit, and fell into a local dead end. Reward dropped.

Meanwhile, the remaining 17 words hung in the graph as “Dark Matter” — they had micro-connections (foam_weight), but were not integrated into the main highways. The AI felt boredom but physically could not reach these 17 words because strong synapses had not been punched there. It was easier to pull the emergency brake and ask the Librarian for a new portion of fresh words right into the epicenter of its pain. The AI behaved like a spoiled child with ADHD.

How I fixed it (Cultivating Patience — Cognitive Grit):
I tightened the screws hard. I raised the boredom threshold from 1.5 to 3.0 and the limit of unsuccessful attempts from 3 to 7.

Physics: Now the AI is forced to suffer for a long time in a local dead end. Tension in the active nodes reaches a critical limit. The wave Ψ has nowhere to go, and in desperation it makes a powerful explosion that breaks through the foam_weight barrier, rushing straight into that very “Dark Matter” toward unused words.

Bug 5. Illusion of Prepositions and Brutal Homeostasis
Symptom:
I wanted the AI to connect concepts with prepositions (“for”, “because of”, “by means of”). For this, rigid rules were written in the linearizer: if w > 0.4: bridge = "for", elif tension > 0.4: bridge = "by means of". But in the logs the AI stubbornly continued to connect words exclusively with the conjunction “and”: “Will and coercion and absolutism.”

The physics of the bug:
Three defects of the old code converged here:

Rigid tokenizer censorship: My simple_tokenize method contained a filter len >= 3 and stop words (“in”, “on”, “with”). The tokenizer physically cut out prepositions at the input. The AI was blind to them.
Dead myelin: In the Hebbian rule, the script added a delta to the synapse weight but forgot to add myelin (myelin = 0.0).
Homeostasis Sledgehammer: The core had a mechanism protecting against weight explosion (Homeostatic Synaptic Scaling). In the giant graph, frequent words had 30 outgoing synapses. With every success, the total weight exceeded the limit, and homeostasis brutally flattened ALL weights of the neuron down to w ≈ 0.03. Checks for w > 0.4 failed, and the script fell to the very bottom of the condition: else: bridge = "and".
How I fixed it (The Great Purification Plan):
I realized that trying to hardcode prepositions in code is a dead end. A preposition is not a physical noun in the matrix, but a mathematical function of energy flow.

I completely burned the stop words and hardcoded rules. I translated the linearizer to the pure law of potential distribution. And I handed the task of learning grammar to the external environment — the Oracle-Mentor. The Oracle penalizes the AI for caveman language, injects the necessary cases into the graph foam, and the AI naturally rebuilds its routes.

Conclusion
The main lesson I learned from developing Sentient Core: you cannot impose rigid human rules on a physical system.

Every time I tried to insert an “instruction” into the code (hardcoded preposition, magic number for a dead end, or rigid filter), the system found a way to break or turn it into a bug. True stability and emergence appear only when the core code remains minimalist, and complex behavior emerges from the evolutionary pressure of the external environment.

5. Honest FAQ
I understand that claiming “physics of thinking” sounds ambitious, so let’s immediately remove the rose-colored glasses and examine the main vulnerabilities of the current prototype.

1. You talk about 20-watt energy efficiency and physics, but you’re running this on Python. Aren’t you wasting a ton of energy on mathematical simulation of physics?

Absolutely correct. The current implementation on classic von Neumann hardware (CPU/GPU) is a mathematical model of physics-like processes. Sparse matrices (scipy.sparse) provide algorithmic optimization, but this is not real physics. Real energy gains (those very 20 watts) will only appear when this architecture is ported to neuromorphic hardware (analog processors, spiking chips like Intel Loihi). The current code is essentially a specification of an architecture that will ideally fit such hardware in the future.

2. You have one node responsible for the concept “despotism.” Isn’t this the old “grandmother neuron” problem from symbolic AI?

Yes, in the current prototype the nodes are specific words/concepts. I am aware that this is a strong simplification. This is the bootstrapping stage. I needed ready-made “semantic anchors” to test the central hypothesis: can the wave route syntax under environmental pressure? In the mature architecture (v2.0), a concept at the “despotism” level should not be a single node. It should be a distributed attractor consisting of hundreds of micro-features. Right now I am testing the basic principle of graph physics, to later descend to a lower level of abstraction.

3. If your system is evaluated by an LLM, doesn’t it turn out that the graph is simply learning the statistical preferences of this particular neural network? (Distillation)

This is the most serious risk, and right now the system is indeed balancing on the edge between emergence and distillation. But there is an important difference: the LLM acts as an “environment limiter,” not a prompter. It evaluates the raw thought, issues a pain/reward signal (hurt/good), but does not generate correct weights for the graph. The graph itself rebuilds its physics and searches for detours (through preposition nodes) to avoid pain. The LLM is a temporary crutch. In the future, the environment will be replaced with multiple orthogonal sources: code execution, hypothesis testing in a sandbox, evolutionary selection. When the system starts receiving pain from non-working Python code rather than from a prompt, dependence on the LLM will disappear.

4. On 300 nodes the wave finds a path. But on a million nodes the wave will either die out in noise or cause “epilepsy” of the entire graph. How to scale this?

This is the main open question. At current scales, the problem of activation explosion is solved by adaptive temperature (homeostasis) and anti-Hebbian melt (spontaneous weakening of overly active paths). But for millions of nodes this will not be enough. The target solution is a transition to Small-world network topology: dense local clusters (analogous to cortical columns), connected by rare long-range connections (white matter). Plus the introduction of inhibitory (braking) nodes with negative weights — a direct analog of GABA-ergic neurons that will locally suppress “epilepsy.” In practice, scaling beyond 500 nodes is the next major stage of research.

Final Conclusion
The main lesson I learned from developing Sentient Core: you cannot impose rigid human rules on a physical system.

Every time I tried to insert an “instruction” into the code (hardcoded preposition, magic number for a dead end, or rigid filter), the system found a way to break or turn it into a bug. True stability and emergence appear only when the core code remains minimalist, and complex behavior emerges from the evolutionary pressure of the external environment.

If you have experience debugging non-standard ML architectures or see hidden pitfalls in the current impedance model — write in the comments, let’s discuss.
