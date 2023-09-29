# Notes: Computer Systems Architecture

Backup of my digital notebooks for UCLA **COM SCI M151B/EC ENGR M116C: Computer
Systems Architecture**, taken Fall 2023 with [Professor Nader
Sehatbakhsh](https://ssysarch.ee.ucla.edu/nader/).

The class website is publicly available at
https://ssysarch.github.io/ECE_M116C-CS_M151B/F23/index.html.

You can find grading policies and other logistical information in the [slides
for the first lecture](slides/L1-%20Introduction.pdf).


## Markdown Files on VS Code

**Pro tip:** For the best experience, install the [**Markdown All in One**
extension](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one).

**Pro tip:** If you're viewing a source file in VS Code, you can use
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>O</kbd> to jump to a symbol in the current
editor and <kbd>Ctrl</kbd>+<kbd>T</kbd> to jump to a symbol in the entire
workspace. For Markdown, that corresponds to headers, so you can use that to
preview the outline and jump around.

**Pro tip:** If you're viewing these source files on VS Code, you can use
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>V</kbd> to render the Markdown in a
separate tab (or <kbd>Ctrl</kbd>+<kbd>K</kbd> <kbd>V</kbd> to open it to the
side) and read that one.


### Exporting to PDF

There are [many ways to do
this](https://gist.github.com/justincbagley/ec0a6334cc86e854715e459349ab1446),
but I personally use the [**Markdown PDF**
extension](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf)
in VS Code to export my documents. After you install the extension, simply go to
the `.md` file you want to export, open the command palette
(<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>), and search for **Markdown PDF:
Export (pdf)**.


## Contributing

**If you spot any errors or would like to make improvements, feel free to open
an issue or pull request!**

I went out of the way to write notes with raw Markdown and on VS Code as opposed
to using a service like Notion (which I do use for other things!). I just insist
on VS Code for notetaking because here I feel at 100% power with full control
over my key binds, scripts, and extensions -- I go *fast* in lecture.

However, one of the biggest disadvantages of this is that pasting images into my
editor doesn't just upload it to some hidden database I don't need to worry
about like how it works in Notion. Because everything's on my local file system,
pasted images are downloaded as a `.png` file in the directory. To avoid
polluting my repository with countless auto-generated `image.png`,
`image-1.png`, etc. I wrote the [img.py](img.py) script to automate the moving
of images to the central [assets/](assets/) directory. The workflow looks
something like:

1. During lecture, copy an image or take a screenshot of something and paste it
   into the editor I'm working on.
2. This downloads the image into the working directory as something like
   `image.png` and creates a `![](...)` image reference in the Markdown source.
3. During downtime, I can then use the script to move and rename the file to
   something more descriptive, which also automatically updates all references
   to this image in the Markdown files.

```sh
./img.py image.png some-descriptive-name.png
```
