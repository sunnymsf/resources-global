## Accessibility

Buttons must have an accessible name to enable assistive technology to describe the button's purpose. Provide this name using the label attribute and make it a clear call to action, for example, **Edit record**.

If you create an icon-only button using `lightning-button`, provide an accessible name using the `aria-label` or `aria-labelledby` attribute. We recommend that you use one of the attributes but not both.

To provide a text label that's not visible on the screen, use `aria-label`.

<!-- prettier-ignore -->
```html
<lightning-button
    aria-label="Download"
    icon-name="utility:download"
    variant="base"></lightning-button>
```

To associate the button with text from another element, use `aria-labelledby`.

<!-- prettier-ignore -->
```html
<h2 id="downloadLabel">Download Files</h2>
<h3 id="downloadDesc">View and make changes to your files</h3>
<lightning-button
    aria-labelledby="downloadLabel downloadDesc"
    icon-name="utility:download"
    variant="base"></lightning-button>
```

To use `aria-label` with additional descriptive text, use `aria-describedby`.

```html
<lightning-button
  aria-label="Close"
  aria-describedby="descriptionClose"
  icon-name="utility:close"
  variant="base"
></lightning-button>
```

Closing this window resets the form and
returns you back to the main page.

Button provides many variants that add color to a button, which convey different meaning on a button. Use the variants together with clear text on the button to match the meaning you’re trying to convey via color. For example, if you use the destructive button to point out a potential warning, make sure the text communicates the same message.

To inform screen readers that a button is disabled, include the disabled attribute.

Use the following accessibility and aria attributes on `lightning-button`.

| ATTRIBUTE          | TYPE                | DESCRIPTION                                                                                                                                                                                                                                                                                                                                          |
| ------------------ | ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `accesskey`        | `string`            | A shortcut key to activate or place focus on the button.                                                                                                                                                                                                                                                                                             |
| `aria-atomic`      | `boolean`           | Specifies whether the screen reader should always present the live region as a whole, even if only part of the region changes. The default is `false`.                                                                                                                                                                                               |
| `aria-controls`    | `ID reference list` | An element ID or a space-separated list of element IDs whose presence or content is controlled by this button.                                                                                                                                                                                                                                       |
| `aria-describedby` | `ID reference list` | An element ID or a space-separated list of element IDs that provide a descriptive label or description for the button.                                                                                                                                                                                                                               |
| `aria-expanded`    | `boolean`           | Indicates whether a collapsible element that's controlled by the button is expanded or collapsed. To reference the controlled element, use `aria-controls`.                                                                                                                                                                                          |
| `aria-haspopup`    | `token`             | Indicates that the button has an interactive popup element. Valid values are `'true'`, `'dialog'`, `'menu'`, `'listbox'`, `'tree'`, and `'grid'`.                                                                                                                                                                                                    |
| `aria-label`       | `string`            | Provides an assistive label where a visible label can’t be used.                                                                                                                                                                                                                                                                                     |
| `aria-labelledby`  | `ID reference list` | Specifies the ID or list of IDs of the element or elements that contain visible descriptive text to describe the button.                                                                                                                                                                                                                             |
| `aria-live`        | `token`             | Indicates the button can dynamically update without a page reload, and specifies how the change is announced by assistive technologies. Possible values include `off`, `polite`, and `assertive`. The default is `off`. For the screen reader to announce changes when the user is idle, use `polite`. For immediate notifications, use `assertive`. |
|                    |                     |                                                                                                                                                                                                                                                                                                                                                      |

For more information, see the WAI-ARIA Specification.

## Source Code

`lightning-button` is available in the Base Components Recipes GitHub repository. It's transpiled into the `c` namespace so that you can use it in your own projects.
