## Small Language Models for Task Planning in Robotics
<p>
  
#### [ Download Command-steps pairs Dataset ]
* Tabletop Dataset [Download](https://drive.google.com/file/d/1QfZ4A0Fs9ZlbAp0xoM_uzKTo35ryhT7V/view?usp=drive_link)
* Kitchen Dataset [Download](https://drive.google.com/file/d/1vf26Pf4YMrkcmroF-dQMGEP4JJRQZwPJ/view?usp=drive_link)

#### [ Dataset description ]
We build datasets to finetune small LMs for task planning in a single domain, such as kitchen and tabletop environments, via knowledge distillation from GPT3.5, by CoT prompting on it. Our dataset consists of high-level commands and corresponding low-level actionable steps. We name our dataset as COST, COmmand-STeps dataset.

#### [ Note that there are two versions of the prompt templates. ]   
 To allow users to build a dataset for their domain, we propose prompt templates, which are .txt files in the 'code/prompt_templates/fixed_objects or flexible_objects' directory, that can be adaptable to any environment and conditions.

1. Prompt for _fixed objects_   
>  The prompt template when the objects to be used in action steps are fixed. It is designed to generate action steps using only given objects. We use this prompt template to build the COST dataset for a _tabletop_ domain.
2. Prompt for _flexible objects_
> The prompt template when the objects to be used in action steps are flexible. It is designed to generate not only the action steps but also the objects required by the action steps, for the input command. For general real-world environments, such as _kitchen_, we use this prompt template.

---
Let's implement a task planner on your domain, utilizing small LMs.  
---
#### First, Generate your own COmmand-STeps Dataset (COST)
> If you already have command-steps dataset for fine-tuning LMs, you can skip this part.
* The case for _fixed objects_
  1. Save your object list on './datasets/{}/objects.json'.format(your_domain) path.
  2.  Once the object list is ready, enter your OPENAI key into Generate_dataset(fixed_objs).ipynb, and run it to build the COST dataset.
* The case for _flexible objects_
  1. Input the prompt on 'code/prompt_templates/flexible_objects/object_generate_prompt.txt' into LLMs (i.e., GPT3.5), and generate the initial objects list to build the COST dataset.
  2. Once the object list is ready, enter your OPENAI key into _Generate_dataset(flexible_objs).ipynb_, and run it to build the COST dataset.
<br>

#### Second, Fine-tune small LMs with your COST dataset
1. sample description
2. sample description ...
<br>

#### Lastly, Test the fine-tuned small LMs
1. sample description
2. sample description ...
<br>
</p>
