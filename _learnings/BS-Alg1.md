---
title: "Rings, Modules and Galois Theory"
collection: learnings
permalink: /learnings/BS/Alg1
excerpt_separator: <!--more-->
date: 2024-06-28
---
关于一些抽代的复习笔记.
<!--more-->

我们这学期学习抽象代数2, 下面是一些(较为简单的)可泛泛地被认为是抽代的东西的一个小总结, 主要是期末我自己用. 
主要分作如下几部分:
- [Galois理论];
- [模]与[复形];
- [交换代数初步];
- [有限群的线性表示].

上述链接都是我的手写笔记链接或知乎链接.
由于Github库的大小限制, 一些手写的笔记我可能会较为经常地放在知乎上.

## 有限群的表示论

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




