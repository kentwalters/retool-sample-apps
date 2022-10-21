# Clean mode

Clean mode is a module that I add to almost every app where I am both an editor and an end-user. 

It contains a switch, an edit link, and a deprecated text component rendering HTML. The HTML that is rendered conditional hides some Retool-specific elements, like the black header bar with the "edit" button. I like clean apps, and the black bar at the top is unattractive. 

For reference, the CSS that clean mode applies is:
```
<style>._37GzR, ._1kVZf  {
  visibility: {{switch1.value ? 'hidden' : 'visible'}};
} 

{{ switch1.value ? '.retool-canvas-container { margin-top: 0px !important; }' : '' }}

header {
  margin-bottom:0px !important;
}
</style>
```

We have to use a deprecated text component rendered as HTML because the new text component doesn't render HTML and the new HTML component doesn't rendering CSS conditionally.

