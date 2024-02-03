This code creates a simple text editor application using the Tkinter library in Python. The text editor provides basic functionalities such as opening and saving files, cutting, copying, pasting text, and selecting all text.

1. Importing necessary modules:
   - `import tkinter as tk` imports the Tkinter module and aliases it as `tk`.
   - `from tkinter import filedialog` imports the filedialog module from Tkinter for opening and saving files.
2. Function definitions:
   - `open_file()`: This function is called when the user selects the "Open" option from the file menu. It opens a file dialog using `filedialog.askopenfilename()` and retrieves the selected file path. If a file is selected, it opens the file in read mode and inserts its contents into the text widget using `text.insert()`.
   - `save_file()`: This function is called when the user selects the "Save" option from the file menu. It opens a file dialog using `filedialog.asksaveasfilename()` and retrieves the chosen file path. If a file path is provided, it opens the file in write mode and writes the contents of the text widget into the file using `text.get()`.
   - `cut_text()`, `copy_text()`, `paste_text()`: These functions are called when the user selects the respective options from the edit menu. They generate virtual events `"<<Cut>>"`, `"<<Copy>>"`, and `"<<Paste>>"` using `text.event_generate()`. These events correspond to the built-in cut, copy, and paste actions in the text widget.
   - `select_all_text()`: This function is called when the user selects the "Select All" option from the edit menu. It selects all the text in the text widget by adding a selection tag from the start (`"1.0"`) to the end (`tk.END`) of the text widget. It also moves the cursor to the start of the text and scrolls the text widget to ensure the cursor is visible. The `return 'break'` statement is used to prevent further event handling.
3. Creating the GUI:
   - An instance of `Tk()` is created and assigned to the variable `root`.
   - The title of the text editor is set using `root.title()`.
   - A `Text` widget is created and packed into the root window using `text = tk.Text(root)` and `text.pack()`.
4. Creating the menu:
   - A `Menu` widget is created and assigned to the variable `menu` using `menu = tk.Menu(root)`.
   - The menu is configured for the root window using `root.config(menu=menu)`.
5. Creating the file menu:
   - A `Menu` widget is created and assigned to the variable `file_menu` using `file_menu = tk.Menu(menu)`.
   - The file menu is added as a cascade menu to the main menu using `menu.add_cascade(label="File", menu=file_menu)`.
   - The options for the file menu are added using `file_menu.add_command()`. The "Open" option calls the `open_file()` function, the "Save" option calls the `save_file()` function, and the "Exit" option calls `root.quit()` to close the application.
6. Creating the edit menu:
   - A `Menu` widget is created and assigned to the variable `edit_menu` using `edit_menu = tk.Menu(menu)`.
   - The edit menu is added as a cascade menu to the main menu using `menu.add_cascade(label="Edit", menu=edit_menu)`.
   - The options for the edit menu are added using `edit_menu.add_command()`.
  
  https://github.com/Madalacharitavya/TextEditor-Using-Python/assets/102969979/ee4cd089-09e2-4be5-a70b-07b78188ead3

   ## Contributing

Contributions are welcome! Feel free to open issues or pull requests.

## License

This project is licensed under the [MIT License](LICENSE).
