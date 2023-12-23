---
title: "Representation of Finite Groups"
collection: learnings
permalink: /learnings/20231223-rep-of-finite-groups
excerpt_separator: <!--more-->
date: 2023-12-24
---
关于有限群表示论的复习笔记.
<!--more-->

采用结合代数和范畴化的语言.

***Thm.*** 
群表示和群代数上的模本质一样: 给定群 $G$ 以及域 $k$, 则有范畴同构 $k[G]\mathsf{Mod} \cong \mathsf{Rep}_{k}G$.

***Proof.*** 
群代数上的左模自然具有线性结构, 考虑赋予线性结构的函子 $F: k[G]\mathsf{Mod} \to \mathsf{Rep}_ {k}G$, 
- objects: $V \mapsto (\rho,V)$;
- morphisms: $\mathrm{Hom}_ {k[G]\mathsf{Mod}}(V,W) \to \mathrm{Hom}_ {\mathsf{Rep}_ {k}G}(V,W),$
这里objects映射由 $\forall x \in V$, $c \in k$, $cx \mapsto (c1_{G})x$ 诱导, $\forall g$ 对应 $\rho_g: V\to V,\,x\mapsto gx$.

反之,考虑赋予 $V \in \mathsf{Vect}(k)$ 以模结构的函子$H: \mathsf{Rep}_ {k}G \to k[G]\mathsf{Mod}$,
- objects: $(\rho,V) \mapsto V$;
- morphisms: $\mathrm{Hom}_ {\mathsf{Rep}_ {k}G}(V,W) \to \mathrm{Hom}_ {k[G]\mathsf{Mod}}(V,W),$
这里objects映射由 $\forall a \in k[G]$, $v \in V$, $(v,a) \mapsto av$诱导. 此时 $V$ 成为一个左 $k[G]$ 模.

而后依上述定义验证 $FH=\mathrm{id}_ {k[G]\mathsf{Mod}}$, $HF=\mathrm{id}_ {\mathsf{Rep}_ {k}G}$即可.




