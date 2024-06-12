def add_task(tasks, task):
    tasks.append(task)
    print("Task added successfully!")

def remove_task(tasks, task_index):
    if 0 <= task_index < len(tasks):
        del tasks[task_index]
        print("Task removed successfully!")
    else:
        print("Invalid task index!")

def view_tasks(tasks):
    if tasks:
        print("Your tasks:")
        for i, task in enumerate(tasks):
            print(f"{i + 1}. {task}")
    else:
        print("No tasks added yet!")

def main():
    tasks = []

    while True:
        print("\nTODO Application")
        print("1. Add Task")
        print("2. Remove Task")
        print("3. View Tasks")
        print("4. Exit")

        choice = input("Enter your choice: ")

        if choice == "1":
            task = input("Enter the task: ")
            add_task(tasks, task)
        elif choice == "2":
            task_index = int(input("Enter the index of task to remove: ")) - 1
            remove_task(tasks, task_index)
        elif choice == "3":
            view_tasks(tasks)
        elif choice == "4":
            print("Exiting...")
            break
        else:
            print("Invalid choice!")

if __name__ == "__main__":
    main()
