# React_movieApp

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

**React**

```javascript
<Router>
    <>
      <Route path="/" exact component={Home} />
      <Route path="/tv" exact component={TV} />
      <Route path="/search" exact component={Search} />
    </>
</Router>
// path: 어느 URL에서 해당 Route를 render를 할 지
// exact: 정확히 해당 패스여야 한다는 걸 알려준다 - exact를 사용하지않을시 /tv와 /tv/popular이 서로 매칭된다.
// component: Route에 왔을 때 어떤 컴포넌트가 보여질 건지에 대한거야

Fragments( <></> )
// 리액트는 두 개의 컴포넌트를 리턴할 수 없고 Router는 오직 하나의 child만 가질 수 있는데 두개 이상 가질 수 있게 하는 방법

// Hash Router(페이지의 Hash를 사용)
// URL에 #이 포함된다. 구현이 쉽지만 #때문에 웹사이트보다는 앱에 있다는 느낌을 줄 수 있다.
// BrowserRouter( HTML history API 사용 )
// 일반적인 페이지처럼 동작한다. 

<Route path="/tv/popular" render={() => <h1>popular</h1>} />
// React Router에 있는 Composition은 두 개 이상의 Route를 랜더링하는 방식
// 뒤에 component를 쓰는 대신 render를 사용할 수 있다( function이 들어감 )

// URL의 앞부분이 같아서 문제 두개의 랜더 되는 문제
// 이 부분을 고치기 위해 Switch를 사용 <Switch>
// Switch는 한 번에 오직 하나의 Route만 Render하게 해줌
// Redirect 추가

// styled-components
// a태그 대신에 React Router에서 주어진 Link
// 이 링크는 해당 페이지가 내 어플리케이션에 있으면
// 그 곳으로 브라우저한 방식으로 가지 않고 JS의 방식으로 가게 해준다.

// styled-reset
// css를 초기화해서 0의 상태에서 시작하게 하는 것

// withRouter
// 다른 컴포넌트를 감싸는 컴포넌트 
// Router에 props를 전달, 덕분에 다른 컴포넌트와도 연결할 수 있고 Header가 우리가 어디 있는지 알 수 있다.

```
