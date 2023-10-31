# Patterns for html

### Patterns for Defining Class and ID Names from Components
### All components require an ID (except for dynamic ones), while classes are optional

## Button
All buttons are defined using the 'btn-type/name' convention
```html
<button id="btn-submit" class="btn-submit">Send form</button>
<button id="btn-add-item" class="btn-add-item">Add</button>
<button id="btn-delete" class="btn-delete">Delete item</button>
```
For example, when you have two components that both submit to the same page...
```html
<button id="btn-submit-person" class="btn-submit-success">register user</button>
<button id="btn-submit-address" class="btn-submit-success">register address</button>
```

## Input
All inputs are defined using the 'input-type/name' convention
```html
<input id="input-name" class="input" name="userName" type="text">
<input id="input-email" class="input" name="userEmail" type="email">
```
dynamic inputs
```html
<input type="radio" name="address.1" value="address.1">
<input type="radio" name="address.2" value="address.2">
<input type="radio" name="address.3" value="address.3">
```
not dynamic inputs
```html
<input type="radio" name="address.1" id="address.1" value="address.1">
<input type="radio" name="address.2" id="address.2" value="address.2">
<input type="radio" name="address.3" id="address.3" value="address.3">
```

## Ul
All unordered lists (ul) are defined using the 'type/name-items' convention in the plural form, while list items (li) are defined using the 'type-name' convention in the singular form within ul 
 - always use -list from ul
 - always use -item from li
 - example: 
   - users-list(ul) - user-item(li)
   - participants-list(ul) - participant-item(li)

not dynamic items
```html
<ul id="users-list" class="users-list">
    <li id="user-x" class="user-item">user x</li>
    <li id="user-y" class="user-item">user y</li>
</ul>
```
dynamic items
```html
<ul id="users-list" class="users-list">
    <li class="user-item">item 1</li>
    <li class="user-item">item 2</li>
</ul>
```

## Div, Section...
The ID is defined based on the container it belongs to, such as 'user info'
```html
<div id="user-info" class="user-info">
    <section id="section-user-name" class="section-input">
        <label id="label-user-name" class="label-input" for="input-user-name">name</label>
        <input id="input-user-name" class="input-user" type="text">
    </section>

    <section id="section-user-email" class="section-input">
        <label id="label-user-email" class="label-input" for="input-user-email">email</label>
        <input id="input-user-email" class="input-user" type="email">
    </section>
</div>
```