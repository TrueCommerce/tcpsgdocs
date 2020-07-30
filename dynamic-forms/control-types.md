# Dynamic Forms: Control Types

## User Controls

These controls are available to be added to a form for user interaction.

### Button

Displays a clickable button. At least one button must be present on a form for it to be "submittable".

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.

#### HTML
```html
<div class="dynamic-form-control dynamic-form-control__button">
    <button id="__ID__" name="__ID__" type="submit">
        <span>__LABEL__</span>
    </button>
</div>
```

---

### Checkbox

Displays a boolean checkbox.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__checkbox">
    <input id="__ID__" name="__ID__" type="checkbox" />
    <label for="__ID__">
        <span>__LABEL__</span>
    </label>
</div>
```

---

### FileUpload

Displays a file upload control.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__fileupload">
    <label for=__ID__">
        <span>__LABEL__</span>
    </label>
    <input id="__ID__" name=__ID__" type="file" />
</div>
```

---

### Hidden

Not rendered in the UI. This control type is included for backward-compatibility with earlier version of the AMP-based dynamic forms that did not support setting data values in the routing script. It is recommended to use the routing script for setting values wherever possible.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__hidden">
    <input id="__ID__" name="__ID__" type="hidden" />
</div>
```

---

### Text

Displays a read-only block of text. Supports markdown for rendering formatted text.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__text">
    <!-- inner html depends on input markdown -->
</div>
```

---

### TextArea

Displays a multi-line text input.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.
* **Placeholder:** The text displayed inside the input if there is no value.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__textarea">
    <label for="__ID__">
        <span>__LABEL__</span>
    </label>
    <textarea id="__ID__" name="__ID__" placeholder="__PLACEHOLDER__"></textarea>
</div>
```

---

### TextBox

Displays a single-line text input.

#### Properties

* **ID:** Used as the key to store the control's associated with in the session.
* **Label:** The text displayed on the control.
* **Placeholder:** The text displayed inside the input if there is no value.

#### HTML

```html
<div class="dynamic-form-control dynamic-form-control__textbox">
    <label for="__ID__">
        <span>__LABEL__</span>
    </label>
    <input id="__ID__" name="__ID__" placeholder="__PLACEHOLDER__" type="text" />
</div>
```

## Platform Controls

These controls are rendered automatically by the platform based on session state, but are still style-able via custom stylesheets.

### Form Divider

Separates users controls from platform controls in the UI.

```html
<div class="dynamic-form-divider"></div>
```

---

### Back Button

```html
<div class="dynamic-form-control dynamic-form-control__backbutton">
    <button id="$back" name="$back" type="submit" value="__clicked">
        <span>&larr; Back</span>
    </button>
</div>
```

---

### Save and Continue Later Button

```html
<div class="dynamic-form-control dynamic-form-control__savebutton">
    <button id="$back" name="$save" type="submit" value="__clicked">
        <span>Save and Continue Later</span>
    </button>
</div>
```
