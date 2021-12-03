# CB Container Pipeline Examples

This repo has several example branches which can be used by SEs to test different K8s resource configurations in a demo environment.

In order to get started, start by setting up your environment by following the [CBC_Container_CICD_Demo_Env](https://github.com/ncomeau/CBC_Container_CICD_Demo_Env) guide.

## Branches

### _CBC_Container_Demo_
 _Cbcbtl validate_ --> _Post validate results to Slack_ --> _Deploy to microk8s_

_Please see the [README.md](https://github.com/JaBarosin/K8sConfigs/blob/CBC_Container_Demo/README.md) on the [CBC_Container_Demo Branch](https://github.com/JaBarosin/K8sConfigs/tree/CBC_Container_Demo) for the verbose setup and usage instructions_

  * Validate and deploy two different k8s configurations to a microk8s cluster, in an effort to highlight how cbctl can be utilized within a deployment pipeline. The intent of this demo is to first highlight how you can practice good hygiene, by identifying potential vulnerabilities and CBC Policy Violations in the build cycle, enabling a proactive posture and optimization of a CI/CD deployment pipeline.
    * Start with the ***'bad'*** deployment - this deployment contains configurations that violate the demo CB Container Policy rules, and terminates the pipeline prior to the deployment phase.
    * Finish with the ***'good'*** deployment - this deployment successfully completes, devoid of any CBC Container Policy violations, and allows for completion of the deployment pipeline, generating a workload of a static site, which is monitored by CB Container resources.
