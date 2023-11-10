---
title: ViewOptions.display_background_shape property
linktitle: display_background_shape property
articleTitle: display_background_shape property
second_title: Aspose.Words for Python
description: "ViewOptions.display_background_shape property. Controls display of the background shape in print layout view."
type: docs
weight: 10
url: /python-net/aspose.words.settings/viewoptions/display_background_shape/
---

## ViewOptions.display_background_shape property

Controls display of the background shape in print layout view.


```python
@property
def display_background_shape(self) -> bool:
    ...

@display_background_shape.setter
def display_background_shape(self, value: bool):
    ...

```

### Examples

Shows how to hide/display document background images in view options.

```python
# Use an HTML string to create a new document with a flat background color.
html = """
    <html>
        <body style='background-color: blue'>
            <p>Hello world!</p>
        </body>
    </html>"""

doc = aw.Document(io.BytesIO(html.encode('utf-8')))

# The source for the document has a flat color background,
# the presence of which will set the "display_background_shape" flag to "True".
self.assertTrue(doc.view_options.display_background_shape)

# Keep the "display_background_shape" as "True" to get the document to display the background color.
# This may affect some text colors to improve visibility.
# Set the "display_background_shape" to "False" to not display the background color.
doc.view_options.display_background_shape = display_background_shape

doc.save(ARTIFACTS_DIR + "ViewOptions.display_background_shape.docx")
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

