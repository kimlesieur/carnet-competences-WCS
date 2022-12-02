# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
//Basic Todo interactions in React Native

//utils
const randomId = () => Math.random().toString();
const createItem = (title) => ({ id: randomId(), title });
const types = {
  ADD: "ADD",
  REMOVE: "REMOVE",
};

export const actionCreators = {
  add: (title) => ({ type: types.ADD, payload: createItem(title) }),
  remove: (id) => ({ type: types.REMOVE, payload: id }),
};

export const initialState = {
  items: [
    createItem("Click to remove"),
    createItem("Learn React Native"),
    createItem("Write Code"),
    createItem("Ship App"),
  ],
};

// Reducer to manage remove and add an item inside the state object
export function reducer(state, action) {
  switch (action.type) {
    case types.ADD:
      return { ...state, items: [...state.items, action.payload] };
    case types.REMOVE:
      return {
        ...state,
        items: state.items.filter((item) => item.id !== action.payload),
      };
  }
}
// Function component which display an input to add a text todo and a list of todos.
// The destructured function dispatch() will call the defined actions inside the reducer
const App = () => {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <View>
      <Title>To-Do List</Title>
      <Input
        placeholder={"Type a todo, then hit enter!"}
        onSubmitEditing={(title) => dispatch(actionCreators.add(title))}
      />
      <List
        items={state.items}
        onPressItem={(id) => dispatch(actionCreators.remove(id))}
      />
    </View>
  );
};
```

### Utilisation dans un projet ✔️

[Reddit Client](https://github.com/kimlesieur/Reddit-client)

Description :
This Reddit client is a frontend made with React and Redux.
It retrieves public subreddits posts and displays them with their comments below.
No link to a Reddit personal account.

### Utilisation en production si applicable ❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ✔️

Projet client SpeedDating

Description :
Développement d'une application React Native pour un site de e-commerce.

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
