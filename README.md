# Gradio-Tutorial
**Input Components**

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
**Output Components**
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
**Layout Components**
gr.Blocks: High-level container for structuring the interface.
gr.Row: Horizontal grouping of components.
gr.Column: Vertical grouping of components.
gr.Tab: Container for organizing components into tabs.
gr.Group: A flexible container for grouping components.
**Special Components**
gr.Chatbot: Specialized component for displaying chatbot messages.
gr.State: Invisible component for storing temporary state across function calls.

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
