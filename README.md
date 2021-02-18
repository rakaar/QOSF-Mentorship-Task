# Task 2 Submission of QOSF Mentorship Program

## Setup in Linux
**Usage of Python 3.6.9 is recommended**
- Create a virtual environment - `python -m venv env`
- Activate the virtual envrionment made - `source env/bin/activate`
- Install the requirements - `pip install -r requirements.txt`
- Open `QOSF_Task_2.ipynb` in Jupyter Notebook - `jupyter-notebook QOSF_Task_2.ipynb`

## Informal Guide
- The [QOSF_Task_2.ipynb](https://github.com/rakaar/QOSF-Mentorship-Task/blob/master/QOSF_Task_2.ipynb) contains the task
- The same can be viewed on Google colab with outputs at this link - TODO
- Things done in the Task
  - The task has been done using Qiskit, however no APIs of Qiskit were used to implement Error correction directly.
  - The basic assumption has been made that a sender sends Qubits to the receiver, who is applying the CNOT gate. Hence before applying the CNOT gate, the receiver must correct the received Qubits and then apply the CNOT gate, and ensure that resulting state is |00> + |11>/root(2)
  -  Task 2.1 of preparing a Bell state has been using quantum gates provided by Qiskit
  -  In Task 2.2, a function has been prepared which can cause a event with probability p, hence with a probability of p/2 X-gate acts on a Qubit and with a probability of p/2 Z-gate acts on the Qubit
  - To ensure that the above has happened correctly
     - State Vector Simulator has been used to check if Phase has been changed or not
     - Task 2.2 has been applied 100 times to see if the appeared error gates are acting as per the expected probabilities
  - In Task 2.3, Shor's 9 bit code has been used to fix the actions of error gates on both the Qubits. The same has been repeated 100 times to see that the end output is indeed the Bell State we expect.
  - The same Task 2.3 is done with fewer bits in total. In the previous cells, seperate ancillary cells were used for both the Qubits. But both the main Qubits can share the same 8 Ancillia bits. After correcting error in 1 Qubit, the ancillia bits are reset.
  - At the end, I tried to implement Steane's code, efficient one as it uses 7 bits in a logical bit. However, it is incomplete. Missing parts are explained in detail [here](https://github.com/rakaar/QOSF-Mentorship-Task/issues/1).
  - Before finalizing the current notebook, I had done some different things, which were wrong! I have burried them in the mistakes folder of this repo :)
  - A [blog](https://raghav.wtf/2021-02-12-measure-m-outof-n/) written by me on a small issue faced during the task.


