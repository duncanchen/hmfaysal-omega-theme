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

How far will you guess the Principal Component Analysis, PCA, can be traced back? It <a href=
"http://imedea.uib-csic.es/master/cambioglobal/Modulo_V_cod101615/Theory/lit_support/pca_wold.pdf" target="_blacnk">was developed</a> in early 20 century, 1901 to be exactly. PCA started gaining the popularity in 1930s, when it was introduced in the phonology research. Since then, it has been widely adopted in the social science researches. But don’t think PCA is a less rigid methodology because of its popularity in social science. In fact, PCA is derived from solid mathematical methods. Can we explain PCA with as less jargons as possible?

![dimesion-projection](http://bit.ly/1O6zLn6)

## Ananlogy 
Let’s start with an analogy first.  Say we like to study a group of fish, which live inside a tank, by recording their position relative to one another. However there is one problem, we are restricted to use a projector and its projection to collect data.  Luckily we still can place the projector any angle we like. Dimension wise, this condition restrict ourselves using 2 dimensional data to study 3 dimension world, although each of the two dimensions is still made out of the original three dimensions.  Under such a restriction, the projector’s position is big a deal, because a bad position is not able to reveal the relative position among the fish.     

![position](http://bit.ly/1JId4Pz)

We now turn to a real world scenario similar to the analogy. Say we conduct a survey, which consists of 100 questions—a 100-dimensional fish tank. We can perform analytics as 100 variable models, but we rarely do so for a couple of reasons. First, often time a questionnaire is designed to have multiple questions for a same topic. The answers of these question are highly correlated. Not only it will be redundant, it is also lead to large estimate error if highly correlated variables exist. (That’s a topic for another day.) Second, we may believe there are some hidden structures among the variables. Each of the hidden variables is still made of the original variables, however we may be able to explain the data better through the hidden variables, or structure.  Therefore there are two questions: 


1.	Where can be place our projector over the data, so we can preserve great separation among the data? 
2.	How many dimensions does the final projections have? 

## PCA

This is where PCA comes is. PCA belongs to a category of statistical method, called multiple variable analysis. In particular, it is a method of dimension reduction. It solves the problems we proposed the following way: 

1. First to the projector position problem, we need to place the projector, right?  In fact, we don’t. We fix the projector’s position and rotate the data, i.e., the fish tank, instead.  This has the same effect. The rotation of data is merely a coordinate transform from one (basis of the vector space, in linear algebra's terms) to another. Notice in this stage, we have not reduced the dimension yet. 
2. To effectively reduce the dimension, the new coordinates has be orthogonal. Orthogonal coordinates allow us to sort the axes by the difference each axis reveals or account for. As you may have guessed, the number of axes we select is the number of dimensions of the projection. This is why PCA called “Principle”, because it only takes the major coordinates revealing sufficient difference among data. The “Component” in PCA is just another name for coordinate.     


## Summary
So to sum up PCA, it is a dimension reduction method. It greatly simplifies the complexity of the large-dimension problem. The principal components may give us insight of the underlying variable structures, but not guarantee. Because while we have reduce the problem to less dimension, each new dimension, i.e. a principal component, is still a linear combination of all original variables. When original variables evenly appear in new basis, it will still be hard to interpret. To avoid this trouble, Sparse PCA is developed.  We will look into the idea, Sparsity, in next post.     

       


