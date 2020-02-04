# React_movieApp

**React**의 컨셉

- arrow function
```javascript
  > data => data;
  > (a, b) => {return a + b;}
```
- Template Literals
```javascript
  > "hi" + name -> `hi ${name}`
```

- Object Destructuring
```javascript
  const human = {
    name: 'jun',
    lastName: 'uu',
    food: {
      lunch: 'soup',
      dinner: 'steak'
    }
  }
  
  // const name = human.name;
  // const nameLast = human.lastName;
  // const dinner = human.food.dinner;
  
  const {
    name, 
    lastName: nameLast,
    food: {lunch, dinner}
  } = human;
  
  console.log(name, nameLast, dinner);
```

- spread operator
```javascript
  const days = ['mon', 'tues', 'wed'];
  const days2 = ['thu', 'fri', 'sat'];
  
  // const allDays = [days, days2];
  
  const allDays = [...days, ...days2, 'sun'];
  
  console.log(allDays);
  
  const ob = {
    a: 1,
    b: 2
  };
  
  const ob2 = {
    c: 3,
    d: 4
  };
  
  // const allOb = {ob, ob2};
  
  const allOb = {...ob, ...ob2};
  
  console.log(allOb);
```

- Classes
```javascript
  class Human {
    constructor(name, lastName) {
      this.name = name;
      this.lastName = lastName;
    }
  }
  
  const alex = new Human('alex', 'don');
  
  console.log(alex);
  
  class Baby extends Human {
    cry() {
      console.log('uuuuuuuuuuuu');
    }
  }
  
  const baby2 = new Baby('alex', 'don');
  
  console.log(Baby.cry());
```

- Array.map
```javascript
  const days = ['mon', 'tues', 'wed', 'thu', 'fri', 'sat'];
  
  const allDays = days.map((data, index) => `${data} ${index}up`);
  
  console.log(allDays);
```

- Array.filter
```javascript
  const numbers = [32,432,5,5,43,1,3,21,,53,2,532,1,23,321,31];
  
  const numberFilter = numbers.filter(number => number > 50);
  
  console.log(numberFilter);
```

- .forEach .includes .push
```javascript
  const arr = ['hi', 'bye', 'you'];
  
  arr.forEach(number => console.log(number));
  
  arr.push(100);
  
  if(arr.includes('hi')) {
    console.log('hi가 있다.');
  } else {
    console.log('hi가 없다.');
  }
```
