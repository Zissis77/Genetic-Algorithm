# 🚚 Multi-Truck Task Assignment with Genetic Algorithms

This project uses a **Genetic Algorithm (GA)** to assign a set of pickup-and-delivery tasks to a fleet of trucks and optimize each truck's delivery route. It handles constraints such as truck capacity (weight and volume) and time windows for pickups.

---

## 🔧 Features

- Multiple trucks with fixed weight/volume capacity
- Randomly generated pickup/delivery tasks
- Support for pickup/delivery time windows
- **Outer GA**: Assigns tasks to trucks
- **Inner GA**: Optimizes delivery sequence per truck
- Penalty-based cost evaluation for constraint violations

---

## 🧠 How It Works

### 1. **Problem Setup**
- `NUM_TRUCKS = 3`: Number of trucks
- `NUM_TASKS = 30`: Number of pickup-delivery tasks
- Each task has:
  - A pickup node
  - A delivery node
  - Weight and volume
  - A pickup time window

### 2. **Genetic Optimization**

- **Outer Genetic Algorithm**:
  - Each individual represents a task-to-truck assignment.
  - Fitness = sum of costs for all trucks.

- **Inner Genetic Algorithm** (per truck):
  - Builds valid pickup→delivery sequences.
  - Evaluates cost based on:
    - Route distance
    - Capacity violations
    - Pickup-before-delivery rules
    - Time window constraints

---

- `Truck X`: List of node visits in route
- `Cost`: Total travel + penalties
- `Tasks`: Sequence used for routing (each task appears twice: pickup + delivery)

---

## 📦 Requirements

- Python 3.7+
- Libraries:
  - `deap`
  - `numpy`

Install with:

```bash
pip install deap numpy


