# Resource Management Simulation

## Overview
This project simulates the allocation and management of resources (employees, budget) across multiple projects.
## Installation
1. Clone the repository.
2. Install any necessary dependencies by running:
3. pip install -r requirements.txt
## Usage
1. Run the simulation using:
2.    python src/main.py   
## Contributing
 Ayush Dutta
 ## src/resource.py
 class Resource:
    def __init__(self, name, cost):
        self.name = name
        self.cost = cost
        class Project:
    def __init__(self, name, budget):
        self.name = name
        self.budget = budget
        self.resources = []
##src/project.py
    def allocate_resource(self, resource):
        if resource.cost <= self.budget:
            self.resources.append(resource)
            self.budget -= resource.cost
            print(f"Allocated {resource.name} to {self.name}")
        else:
            print(f"Insufficient budget to allocate {resource.name} to {self.name}")
            src/simulation.py
            from project import Project
from resource import Resource

def run_simulation():
    ## Example projects
    project1 = Project("Project A", 1000)
    project2 = Project("Project B", 500)

    # Example resources
    res1 = Resource("Resource 1", 300)
    res2 = Resource("Resource 2", 200)

    # Allocating resources
    project1.allocate_resource(res1)
    project2.allocate_resource(res2)
    project2.allocate_resource(res1)  # This should fail due to budget
        from project import Project
from resource import Resource

def run_simulation():
    # Example projects
    project1 = Project("Project A", 1000)
    project2 = Project("Project B", 500)

    # Example resources
    res1 = Resource("Resource 1", 300)
    res2 = Resource("Resource 2", 200)

    # Allocating resources
    project1.allocate_resource(res1)
    project2.allocate_resource(res2)
    project2.allocate_resource(res1)  #
    This should fail due to budget
   ##src/main.py
   from simulation import run_simulation

if __name__ == "__main__":
    run_simulation()
5. Push to GitHub
git init
git add .
git commit -m "Initial commit of resource management simulation"
   
