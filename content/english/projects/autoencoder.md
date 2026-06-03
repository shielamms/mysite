---
title: "An Autoencoder Neural Network from Scratch"
meta_title: ""
summary: "An autoencoder framework built in Python, featuring modular implementations of various neural network components, as well as a sample autoencoder for images of Nordic runes."
date: 2026-03-17T10:00:00Z
image: "/images/projects/autoencoder_network.jpeg"
categories: ["Machine Learning", "Vision"]
draft: false
---

**Code on Github**: https://github.com/shielamms/Autoencoder-Neural-Network-Framework

### Summary

An autoencoder framework built in Python, featuring modular implementations of various neural network components, as well as a sample autoencoder for images of Nordic runes.


### Background

**What is an autoencoder?**

An Autoencoder is a neural network that learns the features of its input data so that it can be used to reconstruct that data. This means that the output of the neural network aims to be as close to its input as it can. After the model has learned the optimal weights that minimise the error between the output and the input, the output can be discarded and only the resulting encoder model is used for further purposes, like classifying images.

The test data for this framework is the Nordic Runes dataset. It is a set of 7x7 pixel images of the runes of the [Elder Futhark](https://en.wikipedia.org/wiki/Elder_Futhark), an old Germanic alphabet. 