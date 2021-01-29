# Calorie Counting App Plan / Notes

## Data Model

Example Model/Shape: 

```javascript
meal = {
  id: 1,
  description: 'Breakfast', 
  calories: 460
}

model = {
  meals: [],
  showForm: false,
  description: 'Dinner',
  calories: 600,
  // addMode/editMode 
  editId: 3,
  nextId: 1,
}
```

## View Functions - to transform the above data model into html and css 

view - for the whole app
  formView - that will show either show tha add meal button or the form
    fieldSet - for the label & input combination ( for meal and calories)
    buttonSet - for the buttons (save and cancel)
  tableView - for the whole table
    tableHeader - for the table header
    mealsBody - for all of the meal records
      mealRow - for each row of meal
        cell - for each individual cell of each row
      totalRow - for totals row

## Update functions - functions that updates teh apps data model when you interact with the app.

- click the Add meal button
- click the edit/delete buttons of the meal records


- Update/interactions
- click the 'Add meal' button - sets the data models showForm field set to true
- value of 'meal' input to update the value of description field in data model
- value of 'calories' input to update the value of calories field in data model
- click 'Save' button should either add or update the existing meal.
- click 'edit' icon should put the app into edit mode for the meal whose edit icon was clicked
- click 'delete' icon should remove the meal from the list