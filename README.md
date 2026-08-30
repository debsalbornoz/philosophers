<h1 align="center">Philosophers</h1>

<div align="center">
<img alt="Static Badge" src="https://img.shields.io/badge/Status-Finished-green">
<img alt="Static Badge" src="https://img.shields.io/badge/42-Project-blue">
<img alt="Static Badge" src="https://img.shields.io/badge/Language-C-lightgrey">
</div>

## About

42's **Philosophers** project is a hands-on exploration of concurrency and synchronization in programming, based on the well-known **"Dining Philosophers"** problem proposed by Edsger Dijkstra in 1965. The project models the life of philosophers sitting at a table to eat, where each philosopher alternates between three states: thinking, eating, and sleeping. To eat, philosophers rely on forks — a shared, limited resource. The central challenge is making sure every philosopher can carry out their activities without falling into a **deadlock**, a **data race**, or **starvation**.

In this project, each philosopher is represented by a thread, enabling their activities to run concurrently. Careful use of synchronization mechanisms, such as mutexes, ensures the forks are accessed safely and in an orderly way. Managing concurrency correctly is crucial to avoid issues like data races — where multiple threads access the same resource at the same time — and deadlocks, where threads end up blocked waiting on each other indefinitely.

As part of 42's curriculum, this project not only builds technical skills in multithreaded programming, but also encourages thinking about system design and architecture, deepening the understanding of concurrency and the challenges it brings. It's an opportunity to sharpen both programming logic and critical thinking — both essential for building robust, efficient software.

## Concepts

- **Threads** — each philosopher is represented by a thread, allowing the thinking, eating, and sleeping activities to run concurrently.
- **Data race** — occurs when two or more threads access the same variable at the same time. Proper synchronization is implemented to prevent this.
- **Deadlock** — happens when threads become blocked, each waiting on the others. Strategies were applied to enforce a consistent order when acquiring forks, avoiding circular waits.
- **Resource management** — synchronization mechanisms, such as mutexes, are used to ensure the forks are accessed safely and in order.

## Table of Contents

- [Build & Run](#build--run)

## Build & Run

To build the project, run:

```bash
make
```

To run it:

```bash
./philosophers 5 410 200 200
```

The program takes up to 5 arguments:

1. **Number of philosophers**
2. **Time to die** — how long a philosopher can go without eating before dying (in ms)
3. **Time to eat** — how long it takes a philosopher to eat (in ms)
4. **Time to sleep** — how long a philosopher sleeps for (in ms)
5. *(optional)* **Number of meals** each philosopher must eat before the simulation stops

---

<p align="center">Built as part of the 42 curriculum 🖥️</p>
