# qiskit-fall-fest-london

Hands-on Qiskit 2 workshop notebooks for [Qiskit Fall Fest London](https://fallfest.qiskit.london).

## Start here

Open the **Qiskit fundamentals lab** in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/qiskit_fundamentals_lab.ipynb)

1. Sign in to Google Colab. Choose **File → Save a copy in Drive** if you want to keep your work.
2. Run the **Setup** cell first to install and import the packages. A standard CPU runtime is enough for these small simulations.
3. Work through exercises **1–5**, then **7** for your first measurement histogram. Try each exercise before opening the solutions.
4. Continue through the remaining fundamentals exercises, then try the intermediate notebook.

Basic Python knowledge (variables, imports, functions, and lists) helps. Start with the simulator exercises: **you do not need an IBM Quantum account or API key for local simulation**, including fake backends. Real hardware is an optional next step.

## Workshop notebooks

| Notebook | What you will learn | Open in Colab |
| --- | --- | --- |
| [Fundamentals lab](notebooks/qiskit_fundamentals_lab.ipynb) | Gates, superposition, entanglement, measurement, and Qiskit 2 workflows. Start here. | [Open lab](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/qiskit_fundamentals_lab.ipynb) |
| [Fundamentals solutions](notebooks/qiskit_fundamentals_lab_solutions.ipynb) | Expandable answers to check after attempting the exercises. | [Open solutions](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/qiskit_fundamentals_lab_solutions.ipynb) |
| [Intermediate lab](notebooks/intermediate_notebook.ipynb) | DiVincenzo criteria, GHZ states, noise, and hardware experiments. | [Open lab](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/intermediate_notebook.ipynb) |
| [Intermediate solutions](notebooks/intermediate_notebook_solutions.ipynb) | Worked examples for the intermediate lab. | [Open solutions](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/intermediate_notebook_solutions.ipynb) |
| [Hello world on IBM hardware](notebooks/hello-world.ipynb) | IBM's hardware workflow, from a Bell state to a 100-qubit GHZ state. Requires IBM Quantum access and credentials; set up the packages before running. | [Open notebook](https://colab.research.google.com/github/LissanKoirala/qiskit-fall-fest-london/blob/main/notebooks/hello-world.ipynb) |

Exercise notebooks contain blanks for you to complete. Running every cell before filling those blanks can produce errors; work through them one at a time.

## Run locally (optional)

Clone or download this repository, then open a terminal in its directory. Create a fresh virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows, use `python -m venv .venv` and activate it in PowerShell with `.venv\Scripts\Activate.ps1`.

Install the packages used by the labs and launch Jupyter:

```bash
python -m pip install "qiskit[visualization]" qiskit-ibm-runtime qiskit-aer qiskit-qasm3-import jupyter
jupyter notebook notebooks/qiskit_fundamentals_lab.ipynb
```

See the [official Qiskit installation guide](https://quantum.cloud.ibm.com/docs/en/guides/install-qiskit) for supported Python versions and platform-specific help. These labs use Qiskit 2 APIs; older tutorials may use different imports and result formats.

## Common beginner questions

- **`ModuleNotFoundError` or a missing drawing dependency?** Run Setup in the notebook's active environment. If imports still fail after installation, restart the kernel/runtime and rerun Setup.
- **`NameError` in an exercise?** Run the earlier cells in order and complete the exercise's placeholders. A runtime restart clears your variables.
- **Why are the counts different each time?** A shot is one execution and measurement of a circuit. Finite samples fluctuate; an ideal Bell-state circuit gives only `00` and `11`, approximately equally often.
- **Which bit is qubit 0?** When qubits are measured into matching classical bits, qubit 0 is the rightmost bit in a result string. See [Qiskit's bit-ordering guide](https://quantum.cloud.ibm.com/docs/en/guides/bit-ordering).
- **When do I need an IBM account?** When you choose to submit jobs to real hardware. Follow the [IBM Cloud setup guide](https://quantum.cloud.ibm.com/docs/en/guides/cloud-setup); hardware access and queue times depend on your account. Keep API keys out of shared notebooks and outputs.

## Useful resources

- [IBM Quantum Composer](https://quantum.cloud.ibm.com/composer): explore gates with a visual circuit editor.
- [IBM Quantum sign-in](https://quantum.cloud.ibm.com/signin): access your hardware account.
- [Basics of quantum information](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information): build the theory behind the exercises.
- [Simulate with Qiskit SDK primitives](https://quantum.cloud.ibm.com/docs/en/guides/simulate-with-qiskit-sdk-primitives): run small circuits with local Sampler and Estimator implementations.

If you get stuck, [open an issue](https://github.com/LissanKoirala/qiskit-fall-fest-london/issues) with the notebook name, cell, package versions, and error message. Remove credentials before sharing.
