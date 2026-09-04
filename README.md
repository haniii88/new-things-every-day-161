function dailyLog161() {
  const tasks = [
    { name: "Read", completed: true },
    { name: "Exercise", completed: true },
    { name: "Study", completed: false },
    { name: "Practice coding", completed: true },
    { name: "Plan tomorrow", completed: false }
  ];

  cons completed = tasks.filter(task => task.completed).length;
  const pending = tasks.length - completed;
  const completionRate = (completed / tasks.length) * 100;

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalTasks: tasks.length,
    completed,
    pending,
    completionRate: `${completionRate.toFixed(1)}%`
  };

  console.log("Daily Task Report:", report);
}

dailyLog161();
