# Meta-Learning for Few-Shot Image Classification using MAML, Reptile & GAN-based Augmentation

This project explores meta-learning techniques for few-shot image classification using MAML (Model-Agnostic Meta-Learning), Reptile, and a GAN-based data augmentation pipeline. The goal is to improve generalization in extremely low-data scenarios such as 1-shot, 2-shot, 5-shot, and 10-shot learning, as highlighted in recent research.

# 🚀 Project Overview

Traditional deep learning models require large datasets, but real-world tasks often provide only a handful of samples. Meta-learning aims to solve this by training models that can adapt quickly to new tasks with very limited data.

In this project:

A MAML framework is implemented to learn initial parameters that can rapidly adapt with only a few gradient steps.

Reptile, a first-order approximation of MAML, is used to compare stability and convergence behavior.

A GAN is optionally integrated to generate synthetic samples for enhancement in sparse-shot settings.

Experimentation is performed on MNIST and Fashion-MNIST (F-MNIST) datasets.

# 📚 Datasets & Task Setup
1. MNIST Few-Shot Tasks

Base classes used for meta-training: digits 0–8

Novel class for adaptation: digit 9

Experiments conducted for 1-shot, 2-shot, 5-shot, and 10-shot learning.

Trained meta-models were evaluated on the unseen class with minimal samples.


<img width="404" height="427" alt="image" src="https://github.com/user-attachments/assets/dfe6402c-75a0-4b86-99df-eb3346e7bd45" />


<img width="404" height="427" alt="image" src="https://github.com/user-attachments/assets/cb404dfc-3bae-460d-be27-695d17f1e09c" />



<img width="404" height="427" alt="image" src="https://github.com/user-attachments/assets/1b4f4c7c-789a-4e73-adc9-fa63b436655f" />




# 2. Cross-Dataset Transfer (MNIST → Fashion-MNIST)

To test the adaptability of the meta-learned models:

The model is meta-trained on MNIST (0–9).

Then adapted to Fashion-MNIST, using only a few samples from each new class.

This demonstrates generalization across visually different domains.
<img width="567" height="590" alt="image" src="https://github.com/user-attachments/assets/ebac382f-de27-4c6d-aeff-b470651e8beb" />


# 🧠 What This Project Focuses On

Improving accuracy in extremely low-shot settings.

Comparing baseline, MAML, Reptile, and GAN-enhanced performance.

Studying how meta-learners behave when trained on MNIST but adapted to F-MNIST.

Understanding the stability and convergence of first-order vs second-order meta-learning.

Experimenting with different inner-loop and outer-loop update strategies.

# 📊 Current Results

MAML and Reptile both show strong adaptation performance in single-digit few-shot tasks.

Cross-dataset adaptation (MNIST → F-MNIST) demonstrates meaningful transfer after only a few updates.

GAN-supported augmentation helps stabilize learning in ultra-low (1-shot, 2-shot) setups.
