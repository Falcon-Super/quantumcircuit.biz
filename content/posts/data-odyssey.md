+++
title = 'Data Odyssey: A Personal Journey Through Rust, Docker, and Data Science'
date = 2024-09-18T19:28:39+03:00
draft = false
tags = ["Rust", "Docker", "Apache Arrow", "data science", "CSV", "containerization", "error handling", "modularization"]
categories = ["Data Science", "Programming", "Tools and Technologies"]
+++

In November 2023, I embarked on a deep dive into the world of data science using **Rust**, **Docker**, and **Apache Arrow**. Over the course of sixteen days, I faced challenges ranging from containerization woes to the intricacies of error handling in Rust, all while gaining valuable insights into how these tools can be effectively used for real-world data science projects.

### Day 1: Rust, APIs, and Containerization

I began by setting up my project with **Cargo.toml**, building the necessary components, and diving headfirst into Rust’s error handling system. However, the challenge escalated when I tried to containerize the project using Docker. The initial setup went smoothly, but I quickly ran into roadblocks with how Rust binaries interacted within a Docker container. Despite these early challenges, it was clear that containerization, while offering uniform environments, required careful attention to detail.

### Day 2: Docker Troubleshooting

On Day 2, I confronted Docker execution hurdles. The Rust binaries, although built successfully, didn’t behave as expected inside the container. I dived into the Docker logs, troubleshooting by rebuilding the container several times. Despite the hurdles, I came away with a deepened understanding of cross-environment development and Rust’s behavior in isolated environments.

### Day 3: Rust’s Type System and CSV Handling

Rust’s strict type system reared its head on Day 3 when I encountered an error while working with CSV files. I attempted to write data to a file using Rust’s `?` operator, only to hit a type mismatch between `std::io::Error` and `reqwest::Error`. This forced me to reevaluate my approach, mapping errors to appropriate types and further deepening my understanding of Rust’s error-handling paradigms.

After some troubleshooting, I shifted from using an API for data retrieval to handling CSV files directly. The reliability of static CSV files provided me with a more controlled environment, allowing me to focus on processing the data with Rust.

### Day 4: Local Development and Data Modularization

By Day 4, I transitioned from Docker back to local development, running Rust directly on my MacBook. This switch immediately improved performance, as I no longer needed to manage the overhead of containerization.

I also restructured my project to make it more modular. By splitting it into distinct modules for data concatenation, CSV-to-Arrow conversion, and analysis, I improved both clarity and maintainability. This marked a turning point in the project, enabling smoother development and faster iteration.

### Day 5: Apache Arrow and Data Complexity

The introduction of **Apache Arrow** for handling large datasets was pivotal. Arrow’s columnar format allowed me to scale the data processing tasks efficiently. However, this came with new challenges, particularly related to handling schema mismatches between CSV files and the data structures expected by Arrow. Debugging these issues involved significant trial and error, but by the end of the day, I had a functioning system for converting CSV files to Arrow format.

### Days 6-16: Reflections and New Tools

As the project progressed, I refined my approach to handling structured data. I adopted a new **documentation template** to improve the presentation of my findings, focusing on creating a professional, polished report. Over the following days, I continued to refine both my code and my understanding of Rust’s strengths and limitations when it comes to data science.

---

This "Data Odyssey" has been a remarkable learning experience. It’s shown me the complexities of integrating Rust into data science workflows, the power of modularizing code, and the importance of selecting the right tools for the job. This journey has not only enhanced my technical skills but also reinforced my commitment to tackling challenges head-on.

---

