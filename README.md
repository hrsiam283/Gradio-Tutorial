# Gradio-Tutorial
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
