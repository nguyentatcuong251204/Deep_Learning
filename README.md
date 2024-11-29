```mermaid
sequenceDiagram
    participant User
    participant TaskManager
    participant Database
    participant Notification
    participant Employee
    
    User->>TaskManager: Create Task
    TaskManager->>Database: Create task record
    Database->>TaskManager: Save to database
    TaskManager->>TaskManager: Assign task to employee
    TaskManager->>Notification: Send notification
    Notification->>Employee: Task assigned
    Notification->>User: Task assigned

