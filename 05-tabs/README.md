Tabs React Project is an interactive application designed to display information about various job positions, focusing on both current and previous roles. Built with React, this project showcases the power of dynamic data fetching and state management to render specific job details based on user interaction.

## Features:

### Dynamic Job Information Display:

The application features a detailed view of job positions. By default, information about a single job position is displayed, providing insights into the role's responsibilities, and other relevant details.

### Interactive List Buttons:

On the left side of the application, users are presented with a list of buttons corresponding to different job positions. Clicking on any of these buttons dynamically updates the main display to show information related to the selected job.

### Data Fetching:

The application incorporates data fetching to retrieve job information, demonstrating a practical use case of asynchronous operations in React. This feature ensures that the application can be easily updated or scaled with information stored externally.

### Display All Option:

Besides individual job details, the application offers an option to display information about all listed jobs simultaneously. This functionality provides a comprehensive overview and enhances user experience by allowing comparisons or quick glances at various roles.

## Dynamic Button Generation with .map()

jobs.map((item, index) => {...}):
This line in my App.js iterates over the jobs array using the .map() method. For each item in the jobs array, the .map() method executes the arrow function provided as its argument. The arrow function returns a button for each job item.

## Button Element

<button key={item.id} onClick={() => setValue(index)} className={job-btn ${index === value && 'active-btn'}}>:

For each job item, a button element is created.

key={item.id}: React requires a unique key prop for each child in a list to help identify which items have changed, are added, or are removed.

onClick={() => setValue(index)}: Assigns an onClick event handler to the button that sets the current index using the setValue function. It is meant to update the state to reflect the currently selected job, triggering a UI update to show the corresponding job details.

className={`job-btn ${index === value && 'active-btn'}`}: Sets the class name dynamically based on the condition index === value. If the condition is true (meaning the current job is selected), the button gets an additional class active-btn alongside job-btn.
