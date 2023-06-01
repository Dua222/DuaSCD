import streamlit as st
# Create a list to store tasks
tasks = []

# Create the Streamlit app
def main():
    st.title("To-Do List")

    # Add task input
    task = st.text_input("Add a new task:")
    if st.button("Add"):
        if task:
            tasks.append(task)
            st.success("Task added successfully!")
        else:
            st.warning("Please enter a task.")

    # Display the tasks
    if tasks:
        st.subheader("Tasks:")
        for i, task in enumerate(tasks, start=1):
            st.write(f"{i}. {task}")
    else:
        st.info("No tasks yet.")

    # Delete task
    delete_task = st.text_input("Enter the task number to delete:")
    if st.button("Delete"):
        if delete_task:
            try:
                task_num = int(delete_task)
                if 1 <= task_num <= len(tasks):
                    tasks.pop(task_num - 1)
                    st.success("Task deleted successfully!")
                else:
                    st.warning("Invalid task number.")
            except ValueError:
                st.warning("Please enter a valid task number.")
        else:
            st.warning("Please enter a task number.")

if __name__ == "__main__":
    main()
