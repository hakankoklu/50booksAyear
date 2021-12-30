## The Mythical Man-Month

##### Essays on Software Engineering

##### by Frederick P. Brooks Jr.

* As a rule of thumb, I estimate that a programming product costs at least three times as much as a debugged program with the same function. ... A programming system component costs at least three times as much as a stand-alone program of the same function. The cost may be greater if the system has many components. ... The programming systems product differs from the simple program in all of the above ways. It costs nine times as much. But it is the truly useful object, the intended product of most system programming efforts.

* The challenge and the mission are to find real solutions to real problems on actual schedules with available resources.

* our estimating techniques fallaciously confuse effort with progress, hiding the assumption that people and months are interchangeable.

* Fifth, when schedule slippage is recognized, the natural (and traditional) response is to add human power. Like dousing a fire with gasoline, this makes matters worse, much worse. More fire requires more gasoline, and thus begins a regenerative cycle which ends in disaster.

* So the first false assumption that underlies the scheduling of systems programming is that all will go well, i.e., that each task will take only as long as it "ought" to take.

* Cost does indeed vary as the product of the number of people and the number of months. Progress does not. Hence the person-month as a unit for measuring the size of a job is a dangerous and deceptive myth. It implies that people and months are interchangeable. People and months are interchangeable commodities only when a task can be partitioned among many workers with no communication among them (Fig. 2.1). This is true of reaping wheat or picking cotton; it is not even approximately true of systems programming.

* No parts of the schedule are so thoroughly affected by sequential constraints as component debugging and system test. Furthermore, the time required depends on the number and subtlety of the errors encountered.

* I have been successfully using the following rule of thumb for scheduling a software task: 1/3 planning 1/6 coding 1/4 component test and early system test 1/4 system test, all components in hand.

* Failure to allow enough time for system test, in particular, is peculiarly disastrous. Since the delay comes at the end of the schedule, no one is aware of schedule trouble until almost the delivery date.

* Oversimplifying outrageously, we state Brooks's Law: Adding human power to a late software project makes it later.

* More software projects have gone awry for lack of calendar time than for all other causes combined.

* First, one must say that one does not estimate the entire task by estimating the coding portion only and then applying the ratios. The coding is only one-sixth or so of the problem, and errors in its estimate or in the ratios could lead to ridiculous results.

* No one can criticize a programming system for size per se and at the same time consistently advocate closer integration of hardware and software design.

* Like any cost, size itself is not bad, but unnecessary size is.

* The first moral is clear: Set total size budgets as well as resident-space budgets; set budgets on backing-store accesses as well as on sizes.

* The second area of craftsmanship is space-time trade-offs. For a given function, the more space, the faster. This is true over an amazingly large range.

* The manager can do two things to help their team make good space-time trade-offs. One is to ensure that they are trained in programming technique, not just left to rely on native wit and previous experience.

* Much more often, strategic breakthrough will come from redoing the representation of the data or tables. This is where the heart of a program lies.

* The programmer at wit's end for lack of space can often do best by disentangling themselves from their code, rearing back, and contemplating their data. Representation is the essence of programming.

* Bit by bit, however, they comes to realize that a certain small set of these documents embodies and expresses much of their managerial work. The preparation of each one serves as a major occasion for focusing thought and crystallizing discussions that otherwise would wander endlessly. Its maintenance becomes their surveillance and warning mechanism. The document itself serves as a check list, a status control, and a data base for their reporting.

* Why Have Formal Documents? First, writing the decisions down is essential. Only when one writes do the gaps appear and the inconsistencies protrude. The act of writing turns out to require hundreds of mini-decisions, and it is the existence of these that distinguishes clear, exact policies from fuzzy ones. Second, the documents will communicate the decisions to others. The manager will be continually amazed that policies they took for common knowledge are totally unknown by some member of their team. Since their fundamental job is to keep everybody going in the same direction, their chief daily task will be communication, not decision-making, and their documents will immensely lighten this load.

* In most projects, the first system built is barely usable. It may be too slow, too big, awkward to use, or all three. There is no alternative but to start again, smarting but smarter, and build a redesigned version in which these problems are solved. The discard and redesign may be done in one lump, or it may be done piece-by-piece. But all large-system experience shows that it will be done.

* The fundamental problem with program maintenance is that fixing a defect has a substantial (20–50 percent) chance of introducing another. So the whole process is two steps forward and one step back.

* They find that the total number of modules increases linearly with release number, but that the number of modules affected increases exponentially with release number. All repairs tend to destroy the structure, to increase the entropy and disorder of the system. Less and less effort is spent on fixing original design flaws; more and more is spent on fixing flaws introduced by earlier fixes. As time passes, the system becomes less and less well-ordered. Sooner or later the fixing ceases to gain any ground. Each forward step is matched by a backward one. Although in principle usable forever, the system has worn out as a base for progress. Furthermore, machines change, configurations change, and user requirements change, so the system is not in fact usable forever. A brand-new, from-the-ground-up redesign is necessary.

* How does one control a big project on a tight schedule? The first step is to have a schedule. Each of a list of events, called milestones, has a date.

* For picking the milestones there is only one relevant rule. Milestones must be concrete, specific, measurable events, defined with knife-edge sharpness. Coding, for a counterexample, is "90 percent finished" for half of the total coding time. Debugging is "99 percent complete" most of the time. "Planning complete" is an event one can proclaim almost at will. Concrete milestones, on the other hand, are 100-percent events. "Specifications signed by architects and implementers," "source coding 100 percent complete, keypunched, entered into disk library," "debugged version passes all test cases." These concrete milestones demark the vague phases of planning, coding, debugging. It is more important that milestones be sharp-edged and unambiguous than that they be easily verifiable by the boss. Rarely will a person lie about milestone progress, if the milestone is so sharp that they can't deceive themselves.

* All software construction involves essential tasks, the fashioning of the complex conceptual structures that compose the abstract software entity, and accidental tasks, the representation of these abstract entities in programming languages and the mapping of these onto machine languages within space and speed constraints.

* the time has come to address the essential parts of the software task, those concerned with fashioning abstract conceptual structures of great complexity. I suggest:
    * Exploiting the mass market to avoid constructing what can be bought. 
    * Using rapid prototyping as part of a planned iteration in establishing software requirements.
    * Growing software organically, adding more and more function to systems as they are run, used, and tested.
    * Identifying and developing the great conceptual designers of the rising generation.

* The essence of a software entity is a construct of interlocking concepts: data sets, relationships among data items, algorithms, and invocations of functions. This essence is abstract, in that the conceptual construct is the same under many different representations.

* I believe the hard part of building software to be the specification, design, and testing of this conceptual construct, not the labor of representing it and testing the fidelity of the representation.

* If this is true, building software will always be hard. There is inherently no silver bullet.

* the inherent properties of this irreducible essence of modern software systems: complexity, conformity, changeability, and invisibility.

* Complexity. Software entities are more complex for their size than perhaps any other human construct, because no two parts are alike

    * The complexity of software is an essential property, not an accidental one. Hence descriptions of a software entity that abstract away its complexity often abstract away its essence.

    * Many of the classical problems of developing software products derive from this essential complexity and its nonlinear increases with size. From the complexity comes the difficulty of communication among team members, which leads to product flaws, cost overruns, schedule delays. From the complexity comes the difficulty of enumerating, much less understanding, all the possible states of the program, and from that comes the unreliability. From the complexity of the functions comes the difficulty of invoking those functions, which makes programs hard to use. From complexity of structure comes the difficulty of extending programs to new functions without creating side effects. From complexity of structure comes the unvisualized states that constitute security trapdoors.

    * No such faith comforts the software engineer. Much of the complexity they must master is arbitrary complexity, forced without rhyme or reason by the many human institutions and systems to which their interfaces must conform. These differ from interface to interface, and from time to time, not because of necessity but only because they were designed by different people, rather than by God.

* Changeability. The software entity is constantly subject to pressures for change.

* Invisibility. Software is invisible and unvisualizable.

    * The reality of software is not inherently embedded in space. Hence it has no ready geometric representation in the way that land has maps, silicon chips have diagrams, computers have connectivity schematics.

* High-level languages. Surely the most powerful stroke for software productivity, reliability, and simplicity has been the progressive use of high-level languages for programming. Most observers credit that development with at least a factor of five in productivity, and with concomitant gains in reliability, simplicity, and comprehensibility.

* Inference engine technology is developed in an application independent way, and then applied to many uses. One can justify much more effort on the inference engines.

* the power of such systems does not come from ever-fancier inference mechanisms, but rather from ever-richer knowledge bases that reflect the real world more accurately.

* Requirements refinement and rapid prototyping. The hardest single part of building a software system is deciding precisely what to build. No other part of the conceptual work is so difficult as establishing the detailed technical requirements, including all the interfaces to people, to machines, and to other software systems. No other part of the work so cripples the resulting system if done wrong. No other part is more difficult to rectify later.

* I would go a step further and assert that it is really impossible for clients, even those working with software engineers, to specify completely, precisely, and correctly the exact requirements of a modern software product before having built and tried some versions of the product they are specifying.

* any software system should be grown by incremental development. That is, the system should first be made to run, even though it does nothing useful except call the proper set of dummy subprograms. Then, bit by bit it is fleshed out, with the subprograms in turn being developed into actions or calls to empty stubs in the level below.

* The fate of WIMP: Obsolescence. Despite its excellencies, I expect the WIMP interface to be a historical relic in a generation. Pointing will still be the way to express nouns as we command our machines; speech is surely the right way to express the verbs. Tools such as Voice Navigator for the Mac and Dragon for the PC already provide this capability.

* The distinctive concerns of software engineering are today exactly those set forth in Chapter 1:
    * How to design and build a set of programs into a system
    * How to design and build a program or a system into a robust, tested, documented, supported product
    * How to maintain intellectual control over complexity in large doses.
