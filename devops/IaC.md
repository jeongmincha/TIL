## What is IaC (Infrastructure as Code)?

I saw an instructional video at [https://www.youtube.com/watch?v=zWw2wuiKd5o](https://www.youtube.com/watch?v=zWw2wuiKd5o)

- first thing to do: build an application on Kubernetes
- basic infrastructure: k8s application stack + VM -> VPC (Virtual Private Cloud)
- test phrase: create a whole new environment that mimics the development environment.
    - case 1: I forgot to document one of the config switches that I've changed.
    - case 2: the platform is different in how it handles provisioning infrastructure.
    - -> in these cases, the application and the test won't work the same way.
- Infrastructure automation approaches
- Approach 1: Imperative approach
    - define step-by-step how to get the infrastructure into a certain state.
    - Usually use a CLI along with a bash script
        - cli create k8s ... cli create VM ... cli create VPC ....
    - complexity comes when tear down VMs, environements, scale-up or down
        - everytime have to write custom scripts
        - doesn't scale well
- Approach 2: Declarative approach
    - ex. Terraform
    - define the final state of the infrastructure, and the provider handle the rest.
        - ex. just config map for k8s resource, VM resource, VPN resource
- Imperative vs Declarative
    - In imperative way, one script run → one environment will be made
        - error handling → have to  tear down the steps
    - In a declarative way, no matter how many times I run the script, I end up with the exact same infrastructure.
- What is DevOps?
    - write codes → test → deploy → ....
    - let's say, one team with a good agile devops workflow and legacy infrastructure
    - they have to open a ticket every time they want to get a new VM
        - this legacy infrastructure → hold them back
    - IaC allows you to treat your infrastructure with the same level of quality that you treat your code.
- Immutable vs Mutable infrastructure
    - with immutable approach
        - every time you want to make a change to the infrastructure, you bring up a brand new environment alongside the old one.
        - and then, once you verify that they're both working and you can bring down the older version.