# SelfAI: Building a Self-Training AI System with LLM Agents


<p align="center">
    📖 <a href="https://arxiv.org/pdf/2501.04227">Paper</a> 
    | 📂 <a href="https://github.com/XiaoXiao-Woo/SelfAI">Codes</a> 
    | 💻 <a href="https://github.com/XiaoXiao-Woo/SelfAI">Software</a>
</p>

----

## ⛴️ Overview:


* SelfAI is a self-training AI system that leverages LLM agents to manage the training process autonomously, tailored to meet the specific needs of researchers. It features customized LLM experts capable of accelerating experimental workflows based on user requirements, focusing on experimental objectives such as method comparisons, ablation studies, and detailed discussions.

* The system implements an experimental management framework that features zero-code parallelization, experiment tracking, and analysis, seamlessly executing diverse experimental configurations without the need for additional code modifications or incurring runtime overhead. Finally, SelfAI significantly reduces researchers' operational burden while accelerating discovery time.


## 🌟 Features
* 👨‍🔬👩‍🔬 User Agent: A specialized LLM module that interprets natural language instructions to generate optimized experimental configurations. It maintains continuous dialogue with researchers through an interactive interface, enabling real-time refinement of experimental parameters based on user feedback and domain-specific requirements.

* 👨‍💻:man_technologist::man_technologist: Engineering Agent: An automated training orchestrator that executes model training with hyper-parameters optimized by Thought Agent. It incorporates advanced experimental management capabilities, including dynamic resource allocation and parallelization support, while maintaining comprehensive experiment tracking and reproducibility.

* 🤯 Cognitive Agent: The system's cognitive module that performs meta-reasoning across experiments. Key capabilities include:

  * Strategic Planning 🗺️: Designs high-level experimental roadmaps based on research objectives 

  * Hypothesis Generation :pushpin: Formulates testable scientific hypotheses from existing results

  * Causal Inference 🏇🏇🏇 : LLM agents combined with Bayesian analysis to identify parameter-effect relationships

  * Adaptive Learning :mag: : Continuously updates its knowledge base from experimental outcomes

  * Failure Analysis: :fire: Diagnoses and recommends solutions for suboptimal results

  * Knowledge Synthesis 🔎 Integrates domain knowledge with empirical findings to guide future experiments
  
## Publishing Date

We will publish the paper on Arxiv and the software on Github in a few days.


## Installation

### 🆚 VSCode Extension

Due to zero-code parallelization architecture, this system can be used as the VSCode extension to execute various experiments, like `VSCode-Python` extension.



###  🍰 Manual Installation

* Clone the GitHub Repository:

```bash
git clone https://github.com/XiaoXiao-Woo/SelfAI.git
```

* Set up and Activate Python Environment
  
```bash
python -m venv selfai
source selfai/bin/activate
```

* Install the dependencies:

```bash
pip install -r requirements.txt
```

* Run the system:

```bash
udl_cil \
--config-path=$CONFIG_DIR \
--config-name=$CONFIG_NAME \
+command=["accelerate","launch","--main_process_port","$AVAILABLE_PORT","--config_file","$ACCELERATE_CONFIG_FILE"] \
+run_file=$YOUR_EXEC_PYTHON_FILE \
+sampler="$SAMPLER" \
+n_jobs=$N_JOBS \
+max_retry=$MAX_RETRY \
experimental_desc=$EXPERIMENTAL_DESC \
+args.import_path="['$WORK_DIR','models']" \ # $WORK_DIR/models/__init__.py
+args.model_name="$MODEL_NAME" \
```



## LICENSE

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.


## Contact

For any questions or suggestions, please contact the author at 

* Xiao.Wu@mbzuai.ac.ae
* wxwsx1997@gmail.com

