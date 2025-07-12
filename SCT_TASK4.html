<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TaskMaster - To-Do App</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.3/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #6366f1;
            --primary-hover: #4f46e5;
            --completed-color: #9ca3af;
            --sidebar-width: 250px;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f9fafb;
            color: #1f2937;
        }
        
        .sidebar {
            width: var(--sidebar-width);
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            background-color: #ffffff;
            border-right: 1px solid #e5e7eb;
            padding: 1.5rem 0;
            overflow-y: auto;
            z-index: 1000;
        }
        
        .sidebar-header {
            padding: 0 1.5rem 1.5rem;
            border-bottom: 1px solid #e5e7eb;
        }
        
        .main-content {
            margin-left: var(--sidebar-width);
            padding: 2rem;
            min-height: 100vh;
        }
        
        .list-group-item {
            border-left: none;
            border-right: none;
            cursor: pointer;
            transition: background-color 0.2s;
        }
        
        .list-group-item:hover {
            background-color: #f3f4f6;
        }
        
        .list-group-item.active {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .task-item {
            background-color: #ffffff;
            border-radius: 0.5rem;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
            margin-bottom: 1rem;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .task-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .task-item.completed .task-content {
            text-decoration: line-through;
            color: var(--completed-color);
        }
        
        .task-actions {
            display: flex;
            gap: 0.5rem;
        }
        
        .btn-primary {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .btn-primary:hover {
            background-color: var(--primary-hover);
            border-color: var(--primary-hover);
        }
        
        .btn-outline-primary {
            color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .btn-outline-primary:hover {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .date-badge {
            font-size: 0.8rem;
            color: #6b7280;
        }
        
        .empty-state {
            text-align: center;
            padding: 3rem;
            color: #6b7280;
        }
        
        .toast-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1100;
        }
        
        @media (max-width: 768px) {
            .sidebar {
                width: 100%;
                height: auto;
                position: relative;
            }
            
            .main-content {
                margin-left: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Sidebar -->
    <div class="sidebar">
        <div class="sidebar-header">
            <h4 class="mb-0 d-flex align-items-center">
                <i class="bi bi-check2-square me-2 text-primary"></i>
                TaskMaster
            </h4>
        </div>
        <div class="p-3">
            <div class="input-group mb-3">
                <input type="text" id="new-list-input" class="form-control" placeholder="New list name">
                <button class="btn btn-primary" id="add-list-btn">
                    <i class="bi bi-plus"></i>
                </button>
            </div>
            <div class="list-group" id="lists-container">
                <a href="#" class="list-group-item list-group-item-action active" data-list-id="default">
                    <i class="bi bi-house-door me-2"></i> My Tasks
                </a>
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <div class="main-content">
        <div class="d-flex justify-content-between align-items-center mb-4">
            <h2 id="current-list-title">My Tasks</h2>
            <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#add-task-modal">
                <i class="bi bi-plus-lg me-1"></i> Add Task
            </button>
        </div>

        <div id="tasks-container">
            <!-- Tasks will be added here dynamically -->
            <div class="empty-state" id="empty-state">
                <i class="bi bi-clipboard-check fs-1 mb-3"></i>
                <h4>No tasks yet</h4>
                <p>Add your first task to get started</p>
                <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#add-task-modal">
                    <i class="bi bi-plus-lg me-1"></i> Add Task
                </button>
            </div>
        </div>
    </div>

    <!-- Add Task Modal -->
    <div class="modal fade" id="add-task-modal" tabindex="-1" aria-labelledby="add-task-modal-label" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="add-task-modal-label">Add New Task</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="add-task-form">
                        <input type="hidden" id="task-list-id" value="default">
                        <div class="mb-3">
                            <label for="task-title" class="form-label">Task Title</label>
                            <input type="text" class="form-control" id="task-title" required>
                        </div>
                        <div class="mb-3">
                            <label for="task-description" class="form-label">Description (Optional)</label>
                            <textarea class="form-control" id="task-description" rows="3"></textarea>
                        </div>
                        <div class="row mb-3">
                            <div class="col">
                                <label for="task-date" class="form-label">Date</label>
                                <input type="date" class="form-control" id="task-date">
                            </div>
                            <div class="col">
                                <label for="task-time" class="form-label">Time</label>
                                <input type="time" class="form-control" id="task-time">
                            </div>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancel</button>
                    <button type="button" class="btn btn-primary" id="save-task-btn">Add Task</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Edit Task Modal -->
    <div class="modal fade" id="edit-task-modal" tabindex="-1" aria-labelledby="edit-task-modal-label" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="edit-task-modal-label">Edit Task</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="edit-task-form">
                        <input type="hidden" id="edit-task-id">
                        <input type="hidden" id="edit-task-list-id">
                        <div class="mb-3">
                            <label for="edit-task-title" class="form-label">Task Title</label>
                            <input type="text" class="form-control" id="edit-task-title" required>
                        </div>
                        <div class="mb-3">
                            <label for="edit-task-description" class="form-label">Description (Optional)</label>
                            <textarea class="form-control" id="edit-task-description" rows="3"></textarea>
                        </div>
                        <div class="row mb-3">
                            <div class="col">
                                <label for="edit-task-date" class="form-label">Date</label>
                                <input type="date" class="form-control" id="edit-task-date">
                            </div>
                            <div class="col">
                                <label for="edit-task-time" class="form-label">Time</label>
                                <input type="time" class="form-control" id="edit-task-time">
                            </div>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cancel</button>
                    <button type="button" class="btn btn-primary" id="update-task-btn">Update Task</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notifications -->
    <div class="toast-container"></div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize data structure
            let data = {
                lists: {
                    'default': {
                        name: 'My Tasks',
                        tasks: []
                    }
                },
                currentListId: 'default'
            };

            // Load data from localStorage if available
            const savedData = localStorage.getItem('taskmasterData');
            if (savedData) {
                try {
                    data = JSON.parse(savedData);
                } catch (e) {
                    console.error('Error loading saved data:', e);
                    // Keep default data structure
                }
            }

            // DOM Elements
            const listsContainer = document.getElementById('lists-container');
            const tasksContainer = document.getElementById('tasks-container');
            const currentListTitle = document.getElementById('current-list-title');
            const newListInput = document.getElementById('new-list-input');
            const addListBtn = document.getElementById('add-list-btn');
            const addTaskForm = document.getElementById('add-task-form');
            const taskListIdInput = document.getElementById('task-list-id');
            const taskTitleInput = document.getElementById('task-title');
            const taskDescriptionInput = document.getElementById('task-description');
            const taskDateInput = document.getElementById('task-date');
            const taskTimeInput = document.getElementById('task-time');
            const saveTaskBtn = document.getElementById('save-task-btn');
            const editTaskForm = document.getElementById('edit-task-form');
            const editTaskIdInput = document.getElementById('edit-task-id');
            const editTaskListIdInput = document.getElementById('edit-task-list-id');
            const editTaskTitleInput = document.getElementById('edit-task-title');
            const editTaskDescriptionInput = document.getElementById('edit-task-description');
            const editTaskDateInput = document.getElementById('edit-task-date');
            const editTaskTimeInput = document.getElementById('edit-task-time');
            const updateTaskBtn = document.getElementById('update-task-btn');
            const emptyState = document.getElementById('empty-state');
            
            // Modals
            const addTaskModal = new bootstrap.Modal(document.getElementById('add-task-modal'));
            const editTaskModal = new bootstrap.Modal(document.getElementById('edit-task-modal'));

            // Initialize the app
            renderLists();
            renderTasks();

            // Event Listeners
            addListBtn.addEventListener('click', addNewList);
            saveTaskBtn.addEventListener('click', saveTask);
            updateTaskBtn.addEventListener('click', updateTask);

            // Functions
            function renderLists() {
                listsContainer.innerHTML = '';
                
                Object.keys(data.lists).forEach(listId => {
                    const list = data.lists[listId];
                    const isActive = listId === data.currentListId;
                    
                    const listElement = document.createElement('a');
                    listElement.href = '#';
                    listElement.className = `list-group-item list-group-item-action ${isActive ? 'active' : ''}`;
                    listElement.dataset.listId = listId;
                    listElement.innerHTML = `
                        <i class="bi bi-list-check me-2"></i> ${list.name}
                        <button class="btn btn-sm text-danger float-end delete-list-btn" data-list-id="${listId}">
                            <i class="bi bi-trash"></i>
                        </button>
                    `;
                    
                    listElement.addEventListener('click', function(e) {
                        if (e.target.closest('.delete-list-btn')) {
                            e.preventDefault();
                            deleteList(listId);
                            return;
                        }
                        
                        e.preventDefault();
                        selectList(listId);
                    });
                    
                    listsContainer.appendChild(listElement);
                });
            }

            function renderTasks() {
                const currentList = data.lists[data.currentListId];
                const tasks = currentList.tasks;
                
                if (tasks.length === 0) {
                    emptyState.style.display = 'block';
                    tasksContainer.innerHTML = '';
                    tasksContainer.appendChild(emptyState);
                    return;
                }
                
                emptyState.style.display = 'none';
                tasksContainer.innerHTML = '';
                
                tasks.forEach(task => {
                    const taskElement = document.createElement('div');
                    taskElement.className = `task-item p-3 ${task.completed ? 'completed' : ''}`;
                    taskElement.dataset.taskId = task.id;
                    
                    let dateTimeDisplay = '';
                    if (task.date || task.time) {
                        dateTimeDisplay = '<span class="date-badge"><i class="bi bi-calendar-event me-1"></i>';
                        if (task.date) dateTimeDisplay += task.date;
                        if (task.time) dateTimeDisplay += ' ' + task.time;
                        dateTimeDisplay += '</span>';
                    }
                    
                    taskElement.innerHTML = `
                        <div class="d-flex justify-content-between align-items-start">
                            <div class="form-check">
                                <input class="form-check-input task-checkbox" type="checkbox" ${task.completed ? 'checked' : ''} id="check-${task.id}">
                                <label class="form-check-label task-content" for="check-${task.id}">
                                    <div class="fw-bold">${task.title}</div>
                                    ${task.description ? `<div class="text-muted small">${task.description}</div>` : ''}
                                    <div class="mt-1">${dateTimeDisplay}</div>
                                </label>
                            </div>
                            <div class="task-actions">
                                <button class="btn btn-sm btn-outline-primary edit-task-btn" data-task-id="${task.id}">
                                    <i class="bi bi-pencil"></i>
                                </button>
                                <button class="btn btn-sm btn-outline-danger delete-task-btn" data-task-id="${task.id}">
                                    <i class="bi bi-trash"></i>
                                </button>
                            </div>
                        </div>
                    `;
                    
                    const checkbox = taskElement.querySelector('.task-checkbox');
                    checkbox.addEventListener('change', function() {
                        toggleTaskCompletion(task.id);
                    });
                    
                    const editBtn = taskElement.querySelector('.edit-task-btn');
                    editBtn.addEventListener('click', function() {
                        openEditTaskModal(task.id);
                    });
                    
                    const deleteBtn = taskElement.querySelector('.delete-task-btn');
                    deleteBtn.addEventListener('click', function() {
                        deleteTask(task.id);
                    });
                    
                    tasksContainer.appendChild(taskElement);
                });
            }

            function selectList(listId) {
                data.currentListId = listId;
                currentListTitle.textContent = data.lists[listId].name;
                renderLists();
                renderTasks();
                saveData();
            }

            function addNewList() {
                const listName = newListInput.value.trim();
                if (!listName) return;
                
                const listId = 'list_' + Date.now();
                data.lists[listId] = {
                    name: listName,
                    tasks: []
                };
                
                newListInput.value = '';
                selectList(listId);
                showToast('List created successfully!', 'success');
            }

            function deleteList(listId) {
                if (Object.keys(data.lists).length <= 1) {
                    showToast('Cannot delete the last list!', 'danger');
                    return;
                }
                
                delete data.lists[listId];
                if (data.currentListId === listId) {
                    selectList(Object.keys(data.lists)[0]);
                } else {
                    renderLists();
                }
                saveData();
                showToast('List deleted successfully!', 'success');
            }

            function saveTask() {
                const title = taskTitleInput.value.trim();
                if (!title) return;
                
                const newTask = {
                    id: 'task_' + Date.now(),
                    title: title,
                    description: taskDescriptionInput.value.trim(),
                    date: taskDateInput.value,
                    time: taskTimeInput.value,
                    completed: false
                };
                
                data.lists[data.currentListId].tasks.push(newTask);
                saveData();
                renderTasks();
                
                // Reset form and close modal
                addTaskForm.reset();
                addTaskModal.hide();
                
                showToast('Task added successfully!', 'success');
            }

            function openEditTaskModal(taskId) {
                const task = data.lists[data.currentListId].tasks.find(t => t.id === taskId);
                if (!task) return;
                
                editTaskIdInput.value = task.id;
                editTaskListIdInput.value = data.currentListId;
                editTaskTitleInput.value = task.title;
                editTaskDescriptionInput.value = task.description || '';
                editTaskDateInput.value = task.date || '';
                editTaskTimeInput.value = task.time || '';
                
                editTaskModal.show();
            }

            function updateTask() {
                const taskId = editTaskIdInput.value;
                const task = data.lists[data.currentListId].tasks.find(t => t.id === taskId);
                if (!task) return;
                
                task.title = editTaskTitleInput.value.trim();
                task.description = editTaskDescriptionInput.value.trim();
                task.date = editTaskDateInput.value;
                task.time =TaskTimeInput.value;
                
                saveData();
                renderTasks();
                editTaskModal.hide();
                
                showToast('Task updated successfully!', 'success');
            }

            function toggleTaskCompletion(taskId) {
                const task = data.lists[data.currentListId].tasks.find(t => t.id === taskId);
                if (!task) return;
                
                task.completed = !task.completed;
                saveData();
                renderTasks();
                
                showToast(task.completed ? 'Task completed!' : 'Task marked as incomplete', 'info');
            }

            function deleteTask(taskId) {
                const taskIndex = data.lists[data.currentListId].tasks.findIndex(t => t.id === taskId);
                if (taskIndex === -1) return;
                
                data.lists[data.currentListId].tasks.splice(taskIndex, 1);
                saveData();
                renderTasks();
                
                showToast('Task deleted successfully!', 'success');
            }

            function saveData() {
                localStorage.setItem('taskmasterData', JSON.stringify(data));
            }

            function showToast(message, type = 'info') {
                const toastContainer = document.querySelector('.toast-container');
                
                const toast = document.createElement('div');
                toast.className = `toast align-items-center text-white bg-${type} border-0`;
                toast.setAttribute('role', 'alert');
                toast.setAttribute('aria-live', 'assertive');
                toast.setAttribute('aria-atomic', 'true');
                
                toast.innerHTML = `
                    <div class="d-flex">
                        <div class="toast-body">
                            ${message}
                        </div>
                        <button type="button" class="btn-close btn-close-white me-2 m-auto" data-bs-dismiss="toast" aria-label="Close"></button>
                    </div>
                `;
                
                toastContainer.appendChild(toast);
                
                const bsToast = new bootstrap.Toast(toast, {
                    autohide: true,
                    delay: 3000
                });
                
                bsToast.show();
                
                // Remove toast from DOM after it's hidden
                toast.addEventListener('hidden.bs.toast', function() {
                    toast.remove();
                });
            }
        });
    </script>
</body>
</html>
