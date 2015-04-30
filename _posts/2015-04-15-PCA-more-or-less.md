---
layout: post
title: "PCA, More or Less"
description: ""
headline: "the missing pieces"
categories: ML
tags: [sparsity,PCA]
imagefeature: draw-on-board.jpg
comments: true
mathjax: true
featured: false
published: true
---

How far would you guess that the Principal Component Analysis (PCA) can be traced back? It <a href=
"http://imedea.uib-csic.es/master/cambioglobal/Modulo_V_cod101615/Theory/lit_support/pca_wold.pdf" target="_blacnk">was developed</a> in the early 20th century…1901 to be exact. PCA started gaining the popularity in 1930s, when it was introduced in phonology research. Since then, it has been widely adopted in social science research. But don’t think PCA is a less rigid methodology because of its popularity in the social sciences. In fact, PCA is derived from solid mathematical methods. Can we explain PCA with as little jargon as possible?


![dimesion-projection](http://bit.ly/1O6zLn6)

## Ananlogy 
Let’s start with an analogy first. Say we would like to study a group of fish inside a tank by recording their positions relative to one another. However, there is one problem: we are restricted to using a projector and its resulting projections to collect data. We can place the projector at any angle we’d like. Dimension-wise, this condition restricts us to using two-dimensional data to study a three-dimensional world, even though each two-dimension projection is still a snapshot of the original three-dimensional reality. Under such a restriction, the projector’s position is big a deal, because a poorly-chosen position would not be able to reveal the relative positions among the fish.     

![position](http://bit.ly/1JId4Pz)

We now turn to a real-world scenario similar to the analogy. Say we conduct a survey, which consists of 100 questions—a 100-dimensional fish tank. We can perform analytics as 100-variable models, but we rarely do so in practice, for a couple of reasons. First, a questionnaire is often designed to have multiple questions for one topic. The answers of these questions are, therefore, highly correlated. Not only would it be redundant, it would also lead to a large estimated error if highly correlated variables exist (a topic for another day). Second, we may believe there are some hidden structures among the variables. Each of the hidden variables is still made of the original variables; however, we may be able to explain the data better through the hidden variables, or structure. Therefore, there are two questions:

1.	Where can we place our “projector” over the data, so as to preserve the greatest separation among the data?
2.	How many dimensions does the final projection have?

## PCA

This is where PCA comes is. PCA belongs to a category of statistical method, called multiple variable analysis. In particular, it is a method of dimension reduction. It solves the problems we proposed the following way: 

1. First to the projector position problem, we need to place the projector, right?  In fact, we don’t. We fix the projector’s position and rotate the data, i.e., the fish tank, instead.  This has the same effect. The rotation of data is merely a coordinate transform from one (basis of the vector space, in linear algebra's terms) to another. Notice in this stage, we have not reduced the dimension yet. 
2. To effectively reduce the dimension, the new coordinates have to be orthogonal. Orthogonal coordinates allow us to sort the axes by the difference each axis reveals or accounts for. As you may have guessed, the number of axes we select is the number of dimensions of the projection. This is why PCA is called “Principle,” because it only takes the major coordinates revealing a sufficient difference among data. The “Component” in PCA is just another name for coordinate.   


## Summary
So to sum up PCA, it is a dimension reduction method. It greatly simplifies the complexity of a large-dimension problem. The principal components may give us insight of the underlying variable structures, but it is not a guarantee. Because, while we have reduced the problem to fewer dimensions, each new dimension-- i.e. a principal component-- is still a linear combination of all the original variables. When original variables appear evenly in the new basis, they are still hard to interpret. To avoid this trouble, Sparse PCA was developed. We will look into the idea, Sparsity, in the next post.
       

