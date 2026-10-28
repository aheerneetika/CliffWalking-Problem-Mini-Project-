Cliff Walking Problem Using SARSA
A mini project demonstrating SARSA
(State--Action--Reward--State--Action), an on-policy
Temporal-Difference reinforcement learning algorithm, through the
classic Cliff Walking environment.
📌 Project Overview
In the Cliff Walking problem, an agent must move through a grid from a
starting position to a goal while avoiding a dangerous cliff. Each move
produces a reward or penalty, and falling off the cliff incurs a large
negative reward. The agent learns a policy through interaction with the
environment.

This project explores how SARSA updates action values based on the
action the agent actually takes, including its exploratory choices.
🎯 Objectives
- Understand the fundamentals of Reinforcement Learning.
- Implement the SARSA on-policy learning algorithm.
- Explore the balance between exploration and exploitation
  using an ε-greedy policy.
- Learn how rewards and penalties influence an agent's behavior.
- Observe how an agent improves its decisions over repeated episodes.
🧠 What Is SARSA?
SARSA is an on-policy Temporal-Difference control algorithm. It updates
the Q-value for a state-action pair using the reward received and the
value of the next state-action pair.

The update rule is:
`\alpha [R_{t+1} + \gamma Q(S_{t+1},A_{t+1}) - Q(S_t,A_t)]`{=tex}\]

Where:

-   **(S_t)**: Current state
-   **(A_t)**: Action selected in the current state
-   **(R\_{t+1})**: Reward received after taking the action
-   **(S\_{t+1})**: Next state
-   **(A\_{t+1})**: Next action selected by the policy
-   **(`\alpha`{=tex})**: Learning rate
-   **(`\gamma`{=tex})**: Discount factor
-   **(Q(S,A))**: Estimated value of taking action (A) in state (S)

Unlike off-policy methods such as Q-learning, SARSA learns using the
next action selected by the current policy.

## 🗺️ Environment

The standard Cliff Walking environment is a grid-world task:

-   **Start:** The agent's starting cell.
-   **Goal:** The destination the agent must reach.
-   **Cliff:** Dangerous cells that produce a large negative reward and
    typically return the agent to the start.
-   **Actions:** Usually up, down, left, and right.
-   **Rewards:** Defined by the environment; in the standard version,
    ordinary steps have a small negative reward, falling off the cliff
    has a large negative reward, and reaching the goal ends the episode.

> Exact grid dimensions, rewards, and environment behavior depend on the
> implementation used in this repository.

## ⚙️ How the Algorithm Works

1.  Initialize the Q-table.
2.  Reset the environment and observe the starting state.
3.  Select an action using an ε-greedy policy.
4.  Execute the action and observe the reward and next state.
5.  Select the next action from the next state using the same policy.
6.  Update the Q-value using the SARSA equation.
7.  Move to the next state-action pair and repeat until the episode
    ends.
8.  Train over multiple episodes and evaluate the learned policy.

## 🧰 Technologies

-   **Language:** Python
-   **Core concept:** Reinforcement Learning
-   **Algorithm:** SARSA (on-policy Temporal-Difference control)
-   **Policy:** ε-greedy action selection
-   **Libraries:** Add the libraries actually used by your
    implementation (for example, NumPy or Matplotlib).

## 🚀 Getting Started

### Prerequisites

-   Python 3.9 or later (adjust to the version used by your project)
-   `pip`

### Installation

1.  Clone this repository:

    ``` bash
    git clone <YOUR_REPOSITORY_URL>
    cd <YOUR_REPOSITORY_FOLDER>
    ```

2.  (Optional but recommended) Create and activate a virtual
    environment:

    **Windows**

    ``` bash
    python -m venv .venv
    .venv\\Scripts\\activate
    ```

    **macOS / Linux**

    ``` bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  Install the dependencies listed in your project:

    ``` bash
    pip install -r requirements.txt
    ```

    If your project does not include a `requirements.txt`, install the
    libraries it imports or create a requirements file first.

### Run the Project

Run the Python entry-point file used in your repository. For example:

``` bash
python main.py
```

Replace `main.py` with your actual script filename. If the project uses
a notebook, open and run the notebook in Jupyter instead.

## 📊 Results

Use this section to document the results produced by your
implementation, such as:

-   Total reward per episode
-   Average reward over a moving window
-   Number of steps required to reach the goal
-   Learned path or final policy
-   Comparison of behavior under different hyperparameters

**Add your actual output, plots, or screenshots here.** Results and
performance depend on the environment settings and training
configuration.

## 🔧 Important Parameters

  -----------------------------------------------------------------------
  Parameter                           Meaning
  ----------------------------------- -----------------------------------
  Learning rate ((`\alpha`{=tex}))    Controls how strongly new
                                      information updates Q-values

  Discount factor ((`\gamma`{=tex}))  Controls the importance of future
                                      rewards

  Exploration rate                    Controls how often the agent
  ((`\epsilon`{=tex}))                explores instead of choosing the
                                      current best-known action

  Episodes                            Number of training episodes
  -----------------------------------------------------------------------

Use the values defined in your code when documenting the final project.

## 📁 Suggested Repository Structure

``` text
cliff-walking-sarsa/
├── README.md
├── requirements.txt
├── main.py                 # Replace with your actual entry-point filename
├── results/                # Optional: plots or screenshots
└── notebooks/              # Optional: Jupyter notebooks
```

This is a suggested structure; adapt it to match your actual files.

## 💡 Key Learnings

-   How an agent learns through interaction with an environment.
-   How SARSA updates Q-values using the next action selected by its
    policy.
-   How ε-greedy selection balances exploration and exploitation.
-   How reward design influences the agent's learned behavior.
-   Why an on-policy method may learn a more cautious path when
    exploratory actions are part of the policy.

## 🔮 Future Improvements

-   Visualize the learned policy and the agent's path.
-   Plot episode rewards and steps over time.
-   Experiment with different learning rates, discount factors, and
    exploration schedules.
-   Compare SARSA with Q-learning in the same environment.
-   Evaluate the learned policy over multiple runs.

## 👩‍💻 Author

**Neetika Aheer**

Mini project developed to strengthen practical understanding of
Reinforcement Learning and SARSA.

------------------------------------------------------------------------
