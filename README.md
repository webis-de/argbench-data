## ArgBench Data
- ArgBench is a benchmark for evaluating instruction-fine-tuned large language models on computational argumentation tasks. The benchmark consists of 57 tasks grouped into 5 skills: argument mining, argument quality assessment, argument perspective assessment, argument reasoning, and argument generation. Two evaluation setups are included in the benchmark: prompting and leave-one-task. The prompting setup evaluates large language models on computational argumentation tasks without fine-tuning them. The leave-ont-out setup evaluates the model’s generalizability to 5 target tasks, while offering the rest tasks as a training set. Each task is split into training, test, and validation.

- tasks: contains the 57 tasks in a json format each task is split into 3 splits (training, val, and test). The files are formatted as follows {task}_{dataset}_{split}_{author}. For example, argument_ranking_ibm_evidence_quality_val_gleize19.
- tasks/metadata: contains metadata like the genre, skills, split files, and used evaluation metric
- preprocess-tasks: the 57 tasks where each instance in each is converted to a json object. An object contains an id, the definition of the task, the input, and the output
- Experiment_splits: contains the split of the tasks for the leave-one-out experiment. For testing on a task, we use  the test set of that task.
Notice that because of Licensing issues, the ArgBench benchmark excludes tasks on Kialo dataset 

- argument_ranking_claim_revisions_skitalinskaya23
- claim_optimization_claim_revisions_skitalinskaya23
- suboptimal_claim_detection_claim_revisions_skitalinskaya23
