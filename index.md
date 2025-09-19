---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: ""
---

# **Biography** 

My name is pronounced [Tzi-Teng Young]. I am a PhD student in the [PLSE Group](https://scs.gatech.edu/programming-languages-software-engineering) at **[Georgia Institute of Technology (GT)](https://www.gatech.edu/)** since 2021. I'm fortunate to be advised by Prof. [**Vivek Sarkar** ](https://vsarkar.cc.gatech.edu/), John P. Imlay, Jr. Dean of the College of Computing. My current research interests are **formal method (proof assistant, especially)**, **compilers** and their applications for anything.

I also took a small gap-year in tech company in 2025. In spring, I worked as an applied scientist intern at [Automated Reasoning Group](https://www.amazon.science/research-areas/automated-reasoning) lead by Dr. [**Daniel Kröning**](https://www.kroening.com/) at **Amazon Web Services (AWS)**, working on a formal verification for ML Compilers ([NKI](https://awsdocs-neuron.readthedocs-hosted.com/en/latest/general/nki/index.html)) using ***[Lean 4](https://github.com/leanprover/lean4) proof assistant***. In the summer, I worked as a compiler engineer at PL & R team of Meta Platforms, Inc., contributing to the great open source **[Triton](https://github.com/triton-lang/triton)** tensor language/compiler (built on [LLVM](https://llvm.org/)/[MLIR](https://mlir.llvm.org/) compiler framework).

Before joining Georgia Tech, I spent my undergraduate time at **[Shanghai Jiao Tong University (SJTU)](https://www.sjtu.edu.cn/)**, major in Computer Science and minor in Music. I was advised by Prof. **[Qinxiang Cao](https://dblp.org/pid/141/1017.html)** and worked on ***compiler correctness*** and ***mathematical logic*** in the ***Coq proof assistant (now renamed to [Rocq](https://rocq-prover.org/))*** from junior to senior year. Prior to that I studied in Prof. **[Xiang Yin](http://xiangyin.sjtu.edu.cn/)**'s' group and worked on ***automata theory*** for control problems during sophomore year.

I'm always open to general research collaboration. <u>Feel free to reach out if you'd like to work on the problems I listed below or your ideas together.</u>

Here is my **[CV](./cv/CV_ZitengYang.pdf)**.

**Contact Information:**

- **Email:**  (fun x y z =>x dot y dot z @gmail.com) cs ziteng yang
- [LinkedIn](https://www.linkedin.com/in/ziteng-yang-a149181b5/), [Twitter](https://twitter.com/_ziteng_yang_)

# **Research**

My current major focus (PhD Thesis) is improving methods for **<u>compiler correctness</u>** in different angle, especially using *[formal verification](https://en.wikipedia.org/wiki/Formal_verification)* through *[proof assistant](https://en.wikipedia.org/wiki/Proof_assistant)*. See the detailed problems including other areas I'm investigating or interested below:

**Formal Verification & Certified Compilation (Primary & Thesis Topic)** 

- **[Ongoing]** **Certified Compilation for Tensor Compiler**

- **[[OOPSLA'24](./papers/oopsla24/oopsla24-final.pdf)] [Improving] Verified Instruction Scheduling**: Achieved **<u>the first ever</u>** <u>fully verified</u> instruction scheduling passes in a formally verified compiler. Further exploration are into verified inter-block scheduling. 

- **[Ongoing] Verified Linear Scan Register Allocation**: Implementing an alternative register allocation algorithm in a formally verified compiler instead of graph-coloring algorithm to reduce both compile-time complexity and verification burden.

- **[Intern@Amazon] Lean for ML Compilers** 

- **Q:** How do we improve the general framework for CompCert to make a parallelizing compilation (e.g. Parallelizing loops in GCC -O3 optimization)

- **Q:** How to implement inter-procedural optimizations in a certified compiler? How far is it from current general framework? 

- **Q:** How can undefined behavior (UB) be exploit in a certified compiler [like LLVM did](https://dl.acm.org/doi/10.1145/3062341.3062343)?

- **Q:** How do we ensure that the formal semantics specification of C (source language) and assembly/machine language (target language) in CompCert is correct w.r.t. their language design?

  A: Testing the reference [C interpreter](https://compcert.org/doc/html/compcert.cfrontend.Cexec.html) (verified to follow the semantics) is all we need (existing work by Su can be found). The assembly semantics is already proved to simulate the C semantics.

- **Q:** Correct-by-construction verification using proof assistant guarantees total correctness but requires heavy proof work and much harder to scale, while translation validation of compiler passes like [Alive2](https://dl.acm.org/doi/10.1145/3453483.3454030) is automatic, algorithm independent and works on real-world scenario, but only find false cases. Should we desire both advantages in one method?

**Parallelism & Concurrency** (secondary, trying to find good methods for important problems)

- **[Reading] Data-race problems**
- **[Reading] GPU Programming, Cuda, OpenMP, MLIR, etc.**
- **[Reading] Program Verification with Concurrency**: concurrent separation logic, etc.

**General Theory** (only in spare time, only for pleasure)

- **Computability view of Program Verification and Analysis**: How do we establish a theory in computability view for certified programs annotated with its correctness information like [*Dafny*](https://dafny.org/), *[Viper](https://www.pm.inf.ethz.ch/research/viper.html)*, [*VST-A*](https://dl.acm.org/doi/10.1145/3632911), etc. ? Can we conclude any non-trivial new theorems based on such model?



**Undergraduate Research at SJTU**

- **Compiler Correctness for Annotation Verifier** [Corresponding author is [Dr. Qinxiang Cao](https://dblp.org/pid/141/1017.html)]: 
  
  I worked on investigating correctness theory of a new idea: compiling programs annotated with verification information ([*annotation verifier*](https://dl.acm.org/doi/10.1145/3632911)) and using them as possible optimization hints. I proposed an extended semantic and verification framework and gave a trial on toy language/logic.
  
  After I graduated, this expedition was continued by [Hanzhi Liu](https://scholar.google.com/citations?user=hEUk48QAAAAJ), [Yanning Chen](https://lightquantum.me/), etc. to go beyond toy language using my framework. Expecting some publication(s) later.
  
- **[[IFAC'20](./papers/IFAC2020/IFAC2020-Final-Full.pdf)] Formal Control Theory (Automata Theory)** [Advised by [Xiang Yin](http://xiangyin.sjtu.edu.cn/)]: Investigated the supervisory control problem for timed discrete-event systems (TDES) under partial observation where time was considered as a special event of an automata.

# **Publications**

<u>Program Verification:</u>

- **Ziteng Yang**, Jun Shirako, and Vivek Sarkar. 2024. Fully Verified Instruction Scheduling. Proc. ACM Program. Lang. 8, **OOPSLA**2, Article 299 (October 2024), 26 pages.

  [ [DOI](https://doi.org/10.1145/3689739) l [PDF](./papers/oopsla24/oopsla24-final.pdf) l [Slide](./papers/oopsla24/oopsla24-slides.pdf) ]

<u>Automata Theory:</u> 

- **Ziteng Yang**, Xiang Yin and Shaoyuan Li. “Maximally permissive supervisor control of timed discrete-event systems under partial observation,” in 21st **IFAC** World Congress, 2020.  

  [ [DOI](https://doi.org/10.1016/j.ifacol.2020.12.2318) l [PDF](./papers/IFAC2020/IFAC2020-Final-Full.pdf)  l  [Slide](./papers/IFAC2020/IFAC2020-Slides.pdf) l  [Video Report](https://youtu.be/GtbxR_OKfXU) ]

# **Teaching Experience**

- **Teaching Assistant** for *CS6390@GT: Programming Languages*, 2023 spring, taught by [**Vivek Sarkar**](https://vsarkar.cc.gatech.edu/)
  - The foundational principles of programming languages

- **Teaching Assistant** for *CS4510@GT: Automata and Complexity*, 2022 fall, taught by [Joseph Jaeger](https://faculty.cc.gatech.edu/~josephjaeger/)
  - Intro to Compatibility: regular language and DFA/NFA, context-free language and PDA, Turning Machine, P/NP/co-NP., L/NL, co-NL 
- **Teaching Assistant**  for *MA208@SJTU: Discrete Mathematics (IEEE/AI Honor Class)*, 2020 fall, taught by [Qinxiang Cao](http://jhc.sjtu.edu.cn/people/members/qinxiang-cao.html) .
  - First-order Logic (proof, semantics and soundness), Set Theory as foundation of Mathematics

- **Teaching Assistant** for  *MA239@SJTU: Discrete Mathematics (Zhiyuan Honor Class)*, 2020 fall, taught by [Xiang Yin](http://xiangyin.sjtu.edu.cn/).
  - Logic and deduction, Graph Theory, Set Theory

# **Honors and Scholarships**

**During PhD Program**

- **Conference Travel Grant** by scholarship of PLMW@PLDI’22, San Diego, Jun. 2022

**During Undergraduate Time**

- **Rongchang Scholarship for Science and Technology Innovation, Finalist** (**10,000 CNY**; 10 winners and 10 finalists among university each year) , Oct. 2020
  
  **荣昶科技创新奖学金, 提名奖 (人民币壹万元)**

- **Undergraduate Excellent Scholarship, Third-class** (Top 20%; **500 CNY**), Oct. 2018
  
  **上海交通大学校优奖学金, C等 (人民币伍佰元)**



# **Misc**

- My hometown is [Chongqing](https://youtu.be/yzl4jc9E5GU?si=DSd5Imm1ZIIlUgCE), the [Night City](https://cyberpunk.fandom.com/wiki/Night_City) of China. Do pay a visit.
- I'm a cat person. Here's [my cat](https://youngzt998.github.io/mycat/).
- I love tennis. (But it hurt my bone...)

