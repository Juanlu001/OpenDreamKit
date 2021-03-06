# Deliverable description, as taken from Github issue #62 on 2017-02-28 {.notoc}

- **WP3:** [Component Architecture](https://github.com/OpenDreamKit/OpenDreamKit/tree/master/WP3)
- **Lead Institution:** University of St Andrews
- **Due:** 2016-08-31 (month 12)
- **Nature:** Other
- **Task:** T3.2 (#51)
- **Proposal:** [p.43](https://github.com/OpenDreamKit/OpenDreamKit/raw/master/Proposal/proposal-www.pdf)
- **Final report:** due 2017-02-28

**SCSCP** stands for the **Symbolic Computation Software Composability Protocol** - the remote procedure call framework by which different software components (primarily mathematical software systems) may offer computational services to a variety of possible clients using the [OpenMath](http://www.openmath.org/) encoding both for the data and protocol instructions (see the [**SCSCP specification**](http://www.symbolic-computing.org/scscp) for further details). 

SCSCP has been developed in the EU FP6 project 026133 [SCIEnce - Symbolic Computation Infrastructure for Europe](http://www.symbolic-computing.org/). In the duration of the project (2006-2011) and subsequent years, several native CAS implementations of SCSCP client and server, and also APIs for Java, C and C++ had appeared (see the complete list [here](http://www.symbolic-computing.org/)). However, there were no Python OpenMath SCSCP implementations (except a prototype quality client supporting only lists of integers) and that hindered further extension of the SCSCP framework.

In this deliverable, we have extended support for SCSCP to other relevant systems involved in the project. This builds foundation to D3.9 "Semantic-aware Sage interface to GAP" (#68) and other activities outlined in our paper ["Interoperability in the OpenDreamKit Project: The Math-in-the-Middle Approach"](https://dx.doi.org/10.1007/978-3-319-42547-4_9) (Intelligent Computer Mathematics. CICM 2016. Lecture Notes in Computer Science, vol 9791. Springer). More specifically, we have achieved the ability to communicate using SCSCP protocol to the following systems/languages:
- [x] Python (both versions 2 and 3): via pure pip-installable packages 
  - [x] openmath 
    - PyPI: https://pypi.python.org/pypi/openmath
    - GitHub: https://github.com/OpenMath/py-openmath
  - [x] scscp
    - PyPI: https://pypi.python.org/pypi/scscp
    - GitHub: https://github.com/OpenMath/py-scscp
- [x] SageMath: via Python packages listed above
- [x] LMFDB: via Python packages listed above
- [x] PARI: 
  - [x] support via D4.1 "Python/Cython bindings for PARI and its integration in Sage" (#83)
  - [ ] later via D4.10 "Second version of the PARI Python/Cython bindings" (#84)
- [x] GAP: via (updated versions of) GAP packages:
  - [x] OpenMath
    - Website: https://gap-packages.github.io/openmath/
    - GitHub: https://github.com/gap-packages/openmath
  - [x] SCSCP
    - Website: https://gap-packages.github.io/scscp/
    - GitHub: https://github.com/gap-packages/scscp 
- [x] Singular: via GAP and/or SageMath
- [x] MMT/MathHub: OpenMath and SCSCP client/server implementations in Scala


---
Remarks:
- Relevant tickets in Sage: https://trac.sagemath.org/ticket/19970 and http://trac.sagemath.org/ticket/19971
- In view of https://wbhart.blogspot.co.uk/2016/11/new-computer-algebra-system-oscar_20.html it's desirable to implement OpenMath and SCSCP in Julia and later use Singular through it. 
