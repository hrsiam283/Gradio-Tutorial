# Gradio-Tutorial
**Input Components**

```
gr.Textbox: Input for text.
gr.Number: Input for numeric values.
gr.Slider: Input for selecting a range of values.
gr.Checkbox: Input for a single checkbox.
gr.CheckboxGroup: Input for multiple checkboxes.
gr.Radio: Input for selecting one option from a list.
gr.Dropdown: Input for selecting one or multiple options from a dropdown.
gr.Button: Button to trigger actions.
gr.File: Input for uploading files.
gr.Image: Input for uploading or drawing images.
gr.Video: Input for uploading videos.
gr.Audio: Input for uploading or recording audio.
gr.Dataframe: Input for tabular data.
gr.TextArea: Input for multi-line text.
```
**Output Components**
```
gr.Label: Output for displaying a label or single value.
gr.Text: Output for displaying text.
gr.HighlightedText: Output for displaying highlighted text.
gr.JSON: Output for displaying JSON data.
gr.HTML: Output for displaying raw HTML.
gr.Image: Output for displaying images.
gr.Video: Output for displaying videos.
gr.Audio: Output for playing audio files.
gr.File: Output for downloading files.
gr.Dataframe: Output for displaying tabular data.
gr.Gallery: Output for displaying multiple images.
```
**Layout Components**
```
gr.Blocks: High-level container for structuring the interface.
gr.Row: Horizontal grouping of components.
gr.Column: Vertical grouping of components.
gr.Tab: Container for organizing components into tabs.
gr.Group: A flexible container for grouping components.
```
**Special Components**
```
gr.Chatbot: Specialized component for displaying chatbot messages.
gr.State: Invisible component for storing temporary state across function calls.
```
**gr.Textbox**
```
gr.Textbox(
    label: str = None,       # Text displayed above the textbox.
    value: str = "",         # Initial value of the textbox.
    placeholder: str = "",   # Placeholder text inside the textbox.
    max_lines: int = 1,      # Maximum number of lines for multi-line input.
    visible: bool = True,    # Whether the textbox is visible.
    interactive: bool = True, # Whether the textbox is editable.
    elem_id: str = "",       # Unique ID for targeting the component.
    elem_classes: list = [], # CSS classes to apply to the textbox.
)
```
**gr.Number **

```
gr.Number(
    label: str = None,         # Text displayed above the number input.
    value: float = 0.0,        # Initial value of the number.
    min: float = None,         # Minimum allowed value.
    max: float = None,         # Maximum allowed value.
    step: float = 1.0,         # Step increment when changing value.
    visible: bool = True,      # Whether the number input is visible.
    interactive: bool = True,  # Whether the input is editable.
    elem_id: str = "",         # Unique ID for targeting the component.
    elem_classes: list = [],   # CSS classes to apply.
)
```
**gr.Slider**
```
gr.Slider(
    label: str = None,         # Label text.
    value: float = 0.0,        # Initial value of the slider.
    minimum: float = 0.0,      # Minimum value of the slider.
    maximum: float = 100.0,    # Maximum value of the slider.
    step: float = 1.0,         # Step increment for the slider.
    visible: bool = True,      # Whether the slider is visible.
    interactive: bool = True,  # Whether the slider is interactive.
    elem_id: str = "",         # Unique ID for targeting the slider.
    elem_classes: list = [],   # CSS classes.
)
```
**gr.Checkbox**
```
gr.Checkbox(
    label: str = None,         # Label text for the checkbox.
    value: bool = False,       # Whether the checkbox is checked or not.
    visible: bool = True,      # Whether the checkbox is visible.
    interactive: bool = True,  # Whether the checkbox is interactive.
    elem_id: str = "",         # Unique ID.
    elem_classes: list = [],   # CSS classes to apply.
)
```
**gr.CheckboxGroup  (Input for multiple checkboxes)**
```
gr.CheckboxGroup(
    label: str = None,         # Label text for the checkbox group.
    choices: list = [],        # List of choices for the checkboxes.
    value: list = [],          # List of initially selected values.
    visible: bool = True,      # Whether the group is visible.
    interactive: bool = True,  # Whether the checkboxes are interactive.
    elem_id: str = "",         # Unique ID.
    elem_classes: list = [],   # CSS classes.
)
```

**gr.Radio (Input for selecting one option from a list)**

```
gr.Radio(
    label: str = None,         # Label text for the radio buttons.
    choices: list = [],        # List of options in the radio buttons.
    value: str = None,         # Initially selected value.
    visible: bool = True,      # Whether the radio buttons are visible.
    interactive: bool = True,  # Whether the radio buttons are interactive.
    elem_id: str = "",         # Unique ID.
    elem_classes: list = [],   # CSS classes.
)
```
**gr.Dropdown (Input for selecting one or multiple options from a dropdown)**
```
gr.Dropdown(
    label: str = None,         # Label for the dropdown.
    choices: list = [],        # List of options.
    value: str = None,         # Initially selected value.
    multiselect: bool = False, # Allow multiple selections.
    visible: bool = True,      # Whether the dropdown is visible.
    interactive: bool = True,  # Whether the dropdown is interactive.
    elem_id: str = "",         # Unique ID.
    elem_classes: list = [],   # CSS classes.
)
```
**gr.Button (Button to trigger actions)**
```gr.Button(
    label: str = "Button",      # Label text on the button.
    variant: str = "primary",   # Button style (e.g., "primary", "secondary").
    visible: bool = True,       # Whether the button is visible.
    interactive: bool = True,   # Whether the button is clickable.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
    tooltip: str = "",          # Tooltip text on hover.
    scale: float = 1.0,         # Button size scaling.
)
```
**gr.File (Input for uploading files)**
```
gr.File(
    label: str = None,          # Label text.
    value: any = None,          # Default value or selected file.
    type: str = "file",         # Can be 'file' or 'url' for external links.
    visible: bool = True,       # Whether the file input is visible.
    interactive: bool = True,   # Whether the input is editable.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```
**gr.Image (Input for uploading or drawing images)**
```
gr.Image(
    label: str = None,          # Label text.
    type: str = "file",         # Can be 'file' or 'numpy' for numpy arrays.
    source: str = "upload",     # Image source, can be 'upload', 'webcam', 'drawing'.
    visible: bool = True,       # Whether the image input is visible.
    interactive: bool = True,   # Whether the input is editable.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```




**11. gr.Video (Input for uploading videos)**
```
gr.Video(
    label: str = None,          # Label text.
    type: str = "file",         # Can be 'file' or 'url'.
    visible: bool = True,       # Whether the video input is visible.
    interactive: bool = True,   # Whether the video input is interactive.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```
**12. gr.Audio (Input for uploading or recording audio)**
```
gr.Audio(
    label: str = None,          # Label text.
    type: str = "file",         # Can be 'file' or 'url'.
    visible: bool = True,       # Whether the audio input is visible.
    interactive: bool = True,   # Whether the audio input is interactive.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```
**13. gr.Dataframe (Input for tabular data)**
```
gr.Dataframe(
    label: str = None,          # Label text.
    value: list = [],           # Initial data (list of lists).
    row_count: int = None,      # Number of rows to show initially.
    col_count: int = None,      # Number of columns to show initially.
    headers: list = [],         # Column names for the table.
    datatype: list = [],        # Data types for each column.
    visible: bool = True,       # Whether the table is visible.
    interactive: bool = True,   # Whether the table is editable.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```
**14. gr.TextArea (Input for multi-line text)**
```
gr.TextArea(
    label: str = None,          # Label text.
    value: str = "",            # Initial text value.
    placeholder: str = "",      # Placeholder text inside the textarea.
    max_lines: int = 5,         # Maximum number of lines.
    visible: bool = True,       # Whether the textarea is visible.
    interactive: bool = True,   # Whether the textarea is editable.
    elem_id: str = "",          # Unique ID.
    elem_classes: list = [],    # CSS classes.
)
```









>Return a component in a function
```
import gradio as gr

# Define the interface
with gr.Blocks() as demo:
    inp = gr.Dropdown(['Hafiz', 'Nafiz', 'Dipesh', 'Bayezid'], label="Select a name")
    textbox = gr.Textbox(visible=False, interactive=True, label="Textbox")
    number = gr.Number(visible=False, interactive=True, label="Number")
    dropdown = gr.Dropdown(['Opt 1', 'Opt 2'], visible=False, interactive=True, label="Options")

    # Define the function to update the component visibility
    def component_return(inp):
        if inp == 'Hafiz':
            return gr.update(visible=True, interactive=True), gr.update(visible=False), gr.update(visible=False)
        elif inp == "Nafiz":
            return gr.update(visible=False), gr.update(visible=True, interactive=True), gr.update(visible=False)
        elif inp == "Dipesh":
            return gr.update(visible=False), gr.update(visible=False), gr.update(visible=True, interactive=True)
        else:
            return gr.update(visible=True, interactive=True), gr.update(visible=False), gr.update(visible=False)

    inp.change(component_return,
               inputs=inp,
               outputs=[textbox, number, dropdown])

demo.launch()
```
