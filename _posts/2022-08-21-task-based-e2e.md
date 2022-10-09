---
toc: true
layout: post
description: Summary and Key points in the paper- *Task-based End-to-end Model Learning in Stochastic Optimization*.
categories: [paper]
title: Task-based End-to-end Model Learning in Stochastic Optimization
---

## L1: Simple problem-solution description: 

The core-problem this paper tries to solve is simple - In an ideal world, the input data distribution matches the ground truth and traditional stochastic optimizers can be employed to solve a given objective function. But, as often is the case in real-world, this is unrealistic. Hence, this paper proposes that the neural networks are added as an intermediary to transforming the input data for sequential quadratic programming solvers to better optimize the given objective function. 

## L2: Key Details

1. The proposed algorithm proposes to learn a probabilistic model to produce predictions that when used in a stochastic programming setting, the resulting decisions would be closest to the true distribution
2. Differentiating through the Stochastic Optimization.
   1. This involves computing the Jacobian (of the optimal action wrt the distribution parameters)
   2. Through the [implicit function theorem](https://en.wikipedia.org/wiki/Implicit_function_theorem), $\nabla$ KKT optimality conditions gives a set of equations that can be solved using OptNet(Amos et. al)

## L3: Coming soon(proofs, detailed analysis and future work)

Slightly secretive since it's part of on-going work.