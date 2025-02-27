# Form Hooks

Each form triggers JavaScript events for which is possible to add listeners and perform custom actions.

## On Submit

Triggers before submission allowing to prevent the action.

```js
UIkit.ready(function() {

  // local
  UIkit.util.on('#form-id', 'form:submit', function (e) {
    // e.preventDefault();
  });

  // global
  UIkit.util.on(document, 'yooessentials-form:submit', function (e, ctx) {
    // ctx = {form}
    // e.preventDefault();
  });

})
```

## On Submitted

Triggers after submission, preventing the action is no longer possible.

```js
UIkit.ready(function() {

  // local
  UIkit.util.on('#form-id', 'form:submitted', function (e, ctx) {
    // ctx = {response}
  });

  // global
  UIkit.util.on(document, 'yooessentials-form:submitted', function (e, ctx) {
    // ctx = {form, response}
  });

});
```

## On Submission Error

Trigger on submission error and validation error.

```js
UIkit.ready(function() {

  // local
  UIkit.util.on('#form-id', 'form:submission-error', function (e, ctx) {
    // ctx = {error, errors, validation}
  });

  // global
  UIkit.util.on('#form-id', 'yooessentials-form:submission-error', function (e, ctx) {
    // ctx = {form, error, errors, validation}
  });

});
```
