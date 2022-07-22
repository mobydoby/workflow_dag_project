
Outline: 
- Introduction
    - importance of obserablity in software (access to status and state of programs)
- Benchmarking
    - current observability functions in workflows
- Proposals
    - DAG structure
    - we want to have these specifications:  
    INPUTS:  
    &nbsp;    workflow.show(optional: workflow_id = name:string , optional: dag = on:bool)  
    OUTPUTS:  
    &nbsp;    ->  dict{  
    &nbsp;&nbsp;            workflow_id_1: {  
    &nbsp;&nbsp;&nbsp;                step_1: status,  
    &nbsp;&nbsp;&nbsp;                ...  
    &nbsp;&nbsp;&nbsp;                next_step: "name"  
    &nbsp;&nbsp;            },  
    &nbsp;&nbsp;            ...  
    &nbsp;        }  
    - in order to achieve this, there needs to be a way to keep track of the next steps
    - After this is achieved, another algorithm can use this API to produce a drawing of the information (DAG)