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
    project2.allocate_resource(res1)  # This should fail due to budget
