# Runtime Loop

while True:

    observe()
    load_state()

    tasks = get_tasks()

    if tasks:
        plan(tasks)

    execute_ready_tasks()

    evaluate()

    update_memory()

    improve()

    sleep(interval)