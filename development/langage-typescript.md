# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ✔️
- les classes et les decorators ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```typescript
// Union types
type Place = "home" | "work" | { custom: string };

// Readonly utility type = make all props readonly
type Todo = Readonly<{
  id: number;
  text: string;
  done: boolean;
  place?: Place;
}>;

// Intersection to create a new type based on another one
type CompletedTodo = Todo & { readonly done: true };

// Type a function : take a Todo as param and return a Todo type object
// with the done property toggled
function toggleTodo(todo: Todo): Todo {
  return {
    id: todo.id,
    text: todo.text,
    done: !todo.done,
  };
}
```

### Utilisation dans un projet ✔️

[tapAndGo : A map application to find bicycles station near you, Typescript version](https://github.com/kimlesieur/tapandgo-typescript)

Description :

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- [TypeScript doc](https://www.typescriptlang.org/docs/handbook/decorators.html#:~:text=A%20Decorator%20is%20a%20special,information%20about%20the%20decorated%20declaration.)
- [Understanding decorators - dev.to](https://dev.to/siddharthshyniben/understanding-typescript-decorators-3ifc)

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
  Decorators : approfondir la notion et maitriser le sujet
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
