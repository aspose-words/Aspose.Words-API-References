---
title: CleanupOptions.symbolic_fonts property
linktitle: symbolic_fonts property
articleTitle: symbolic_fonts property
second_title: Aspose.Words for Python
description: "CleanupOptions.symbolic_fonts property. Specifies that symbolic fonts (Symbol, Wingdings, etc...) should be replaced using appropriate Unicode fonts"
type: docs
weight: 601
url: /python-net/aspose.words/cleanupoptions/symbolic_fonts/
---

## CleanupOptions.symbolic_fonts property

Specifies that symbolic fonts (Symbol, Wingdings, etc...) should be replaced using appropriate Unicode fonts.
Default value is ``False``.



```python
@property
def symbolic_fonts(self) -> bool:
    ...

@symbolic_fonts.setter
def symbolic_fonts(self, value: bool):
    ...

```

### Examples

Shows how to replace text formatted with symbolic fonts (Symbol, Wingdings, etc.) with Unicode text.

```python
doc = aw.Document(file_name=MY_DIR + "Rendering.docx")

# Symbolic fonts display characters with glyphs of their own. For example, the "Symbol" font
# displays the U+F057 character as "Ω", so the text loses its meaning without the font.
symbolic_fonts = ["Symbol", "Wingdings"]

def describe(run):
    return f'"{run.text}" ({" ".join(f"U+{ord(c):04X}" for c in run.text)}), font "{run.font.name}"'

paragraphs = []

for node in doc.get_child_nodes(aw.NodeType.RUN, True):
    run = node.as_run()

    if run.font.name not in symbolic_fonts:
        continue

    print(f"Before: {describe(run)}")

    if run.parent_paragraph not in paragraphs:
        paragraphs.append(run.parent_paragraph)

# Replace the symbolic text with the equivalent Unicode text formatted with appropriate Unicode fonts.
cleanup_options = aw.CleanupOptions()
cleanup_options.symbolic_fonts = True
doc.cleanup(cleanup_options)

# The same paragraphs now show the symbols as regular Unicode characters, for example, "Ω" is U+03A9.
for paragraph in paragraphs:
    for run in paragraph.runs:
        run = run.as_run()
        if any(ord(c) > 127 for c in run.text):
            print(f"After: {describe(run)}")

doc.save(file_name=ARTIFACTS_DIR + "CleanupOptions.SymbolicFonts.docx")
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

