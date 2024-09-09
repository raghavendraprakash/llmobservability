## LLM Observability
LLM Observability with Langfuse, an open source LLM engineering platform.

While both application observability and LLM observability share the goal of understanding and monitoring complex systems, the specific techniques, targets, and challenges differ due to the fundamental differences between traditional software applications and large language models. 
LLM observability is an emerging field that aims to provide insights into the behavior of these powerful but often opaque models, enabling better transparency, accountability, and trust in their outputs.

The challenges are different
Application observability deals with distributed systems, handling large volumes of data, and correlating events across multiple components, while LLM observability deals with understanding blackbox model behavior when provided different input contexts, to ensure acceptable degree of certainty.

**Application observability:**
The targets are typically software components, such as microservices, APIs, databases, and infrastructure components.
Relies on techniques like logging, tracing, metrics collection, and distributed tracing to monitor and understand application behavior.
Goal is to ensure reliable and efficient application performance, identify and resolve issues, and optimize resource utilization.

**LLM observability:**
The target is the model behavior itself, including its inputs, prompts, outputs, internal thought processes, and decision-making processes.
Involves techniques like output analysis, attention visualization, probing, and interpretability methods to understand the model's decision-making process and the influence of different input features.
Goal is to understand the model's behavior, identifying potential biases or inconsistencies, and improving transparency and interpretability of the model's outputs.

### Setting up Langfuse
**Pre-requisite**
* Ensure that you have docker runtime installed and running
```
# Clone the Langfuse repository 
git clone https://github.com/langfuse/langfuse.git
cd langfuse
# Start the server and database
docker-compose up
```
Type on the browser address bar: 
```
http://localhost:3000
```

Once the browser shows Langfuse login console, sign up.
Once you logged in, go to Settings, Create API Key, note down, Public Key, Secret Key. You need this to configure in the notebooks that you would be trying out.

### Setting up Jupyter Lab
***Pre-requisite**
* Ensure that you have Python3 (I have Python 3.12.3)
  Check with this command: 
```
%python3 --version
```
Create a venv and install Jupyter Lab

```
python3 -m venv ./.venv
source .venv/bin/activate
pip install --upgrade pip
pip install jupyterlab
# The following command will start Jupyter lab on localhost:8888
jupyter lab
```
Upon issuing the command, the browser should automatically open Jupyter Lab console. If not, type on the browser address bar:
```
http://localhost:8888/lab
```
* Import jupyter notebooks from the cloned repository
* Start experimenting

