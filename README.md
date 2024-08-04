# python-code-for-to-do-lists
tasks = []

def addTask():
    task =  input("Please enter a task: ")
    tasks.append(task)
    print(f"Task '{task}' added to the list.")

def listTasks():
    if not tasks:
        print("There are no tasks currently.")
        for index, task in enumerate(tasks):
            print(f"Task #{index}. {task}")

def deleteTask():
    listTasks()
    try:
        taskToDelete = int(input("Enter the # to delete: "))
        if taskToDelete >= 0 and taskToDelete < len(tasks):
            tasks.pop(taskToDelete)
            print(f"Task {taskToDelete} has been removed.")
        else:
            print(f"Task #{taskToDelete} was not found.")
    except:
        print("invalid input")

if __name__ == "__main__":
    ### create a loop to the app
    print("Welcome to the to do lists app: ")
    while True:
        print("\n")
        print("Please select one of the following options: ")
        print("--------------------------------------------")
        print("1. Add a new task")
        print("2. Delete a task")
        print("3. List tasks")
        print("4. Quit")

        choice = input("enter you choice: ")
        
        if (choice == "1"):
            addTask()
        elif (choice == "2"):
            deleteTask()
        elif (choice == "3"):
            listTasks()
        elif (choice == "4"):
            break
        else:
            print("invalid input. please try again")

print("goodbye")

