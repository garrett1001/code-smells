#Duplicated Code

##Example
In the following two code chunks, we doing something very similar: pulling from the 'tasks' database and then just manipulating the data in two different ways.
```{JavaScript}
componentWillMount() {
    const taskref = firebase.database().ref(`tasks/`);

    taskref.on("value", snapshot => {

      let tasks = snapshot.val();

      let newState = [];

      for(let item in tasks){
        if (tasks[item].completed == false)
        {
          newState.push({
            name: tasks[item].name,
            description: tasks[item].description,
            date: tasks[item].date,
            completed: tasks[item].completed,
            key: item
          });
```
          
```{JavaScript}
componentWillMount() {
      const taskref = firebase.database().ref(`tasks/`);

      taskref.on("value", snapshot => {

        let tasks = snapshot.val();

        let newState = [];

        for(let item in tasks){
          if (tasks[item].completed == false)
          {
            newState.push(
              tasks[item].date);
          }
        }
```
