PROJECT SETUP
npm install
node index.js

DATABASE
Open MongoDB Compass
Create new Database named as taskdb
create collection named as tasks

OUTPUT DATA:
1)ADD TASKS
mutation {
  createTask(input: {
    title: "Big Feature Implementation",
    description: "Implement GraphQL with 20 attributes",
    status: "IN_PROGRESS",
    dueDate: "2025-09-30T00:00:00.000Z",
    priority: "HIGH",
    tags: ["graphql", "backend", "urgent"],
    category: "Feature",
    estimatedHours: "15",
    actualHours: "5",
    progress: "30",
    attachments: ["https://example.com/specs.pdf"],
    createdBy: "Alice",
    assignedTo: "Bob",
    reviewer: "Charlie",
    team: ["Backend Team", "API Team"],
    isRecurring: false,
    recurrencePattern: "WEEKLY"
  }) {
    id
    title
    priority
    tags
    category
    estimatedHours
    actualHours
    progress
    createdBy
    assignedTo
    reviewer
    team
  }
}
2)GET TASKS
query {
  getTasks {
    id
    title
    description
    status
    dueDate
    priority
    tags
    category
    estimatedHours
    actualHours
    progress
    attachments
    createdBy
    assignedTo
    reviewer
    team
    isRecurring
    recurrencePattern
  }
}
3)GET TASK BY ID
query {
  getTaskById(id: "TASK_ID_HERE") {
    id
    title
    description
    status
    dueDate
    priority
    tags
    category
    estimatedHours
    actualHours
    progress
    createdBy
    assignedTo
    reviewer
    team
  }
}
4)DELETE TASK BY ID
mutation {
  deleteTask(id: "TASK_ID_HERE") {
    id
    title
    status
    message
  }
}


COMMANDS FOR DEPLOYMENT
Open Ubuntu/WSL
sudo apt update
sudo apt install ansible -y
ansible --version
cd /mnt/c/Users/<YourWindowsUsername>.....GET INTO YOUR PROJECT FOLDER(Diskname should be in lowercase and use forward slash)
ansible-playbook deploy.yml



