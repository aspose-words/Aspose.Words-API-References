---
title: detect_numbering_with_whitespaces property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify how numbered list items are recognized when document is imported from plain text format"
type: docs
weight: 20
url: /python-net/aspose.words.loading/txtloadoptions/detect_numbering_with_whitespaces/
---

## TxtLoadOptions.detect_numbering_with_whitespaces property

Allows to specify how numbered list items are recognized when document is imported from plain text format.
The default value is true.

If this option is set to false, lists recognition algorithm detects list paragraphs, when list numbers ends with 
either dot, right bracket or bullet symbols (such as "•", "\*", "-" or "o").

If this option is set to true, whitespaces are also used as list number delimiters:
list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.




### Examples

Shows how to detect lists when loading plaintext documents.

```python
# Create a plaintext document in a string with four separate parts that we may interpret as lists,
# with different delimiters. Upon loading the plaintext document into a "Document" object,
# Aspose.Words will always detect the first three lists and will add a "List" object
# for each to the document's "lists" property.
text_doc = textwrap.dedent("""
Full stop delimiters:
1. First list item 1
2. First list item 2
3. First list item 3

Right bracket delimiters:
1) Second list item 1
2) Second list item 2
3) Second list item 3

Bullet delimiters:
• Third list item 1
• Third list item 2
• Third list item 3

Whitespace delimiters:
1 Fourth list item 1
2 Fourth list item 2
3 Fourth list item 3""").lstrip()

# Create a "TxtLoadOptions" object, which we can pass to a document's constructor
# to modify how we load a plaintext document.
load_options = aw.loading.TxtLoadOptions()

# Set the "detect_numbering_with_whitespaces" property to "True" to detect numbered items
# with whitespace delimiters, such as the fourth list in our document, as lists.
# This may also falsely detect paragraphs that begin with numbers as lists.
# Set the "detect_numbering_with_whitespaces" property to "False"
# to not create lists from numbered items with whitespace delimiters.
load_options.detect_numbering_with_whitespaces = detect_numbering_with_whitespaces

doc = aw.Document(io.BytesIO(text_doc.encode("utf-8")), load_options)

if detect_numbering_with_whitespaces:
    self.assertEqual(4, doc.lists.count)
    self.assertTrue(any("Fourth list" in p.get_text() and p.as_paragraph().is_list_item
                        for p in doc.first_section.body.paragraphs))
else:
    self.assertEqual(3, doc.lists.count)
    self.assertFalse(any("Fourth list" in p.get_text() and p.as_paragraph().is_list_item
                         for p in doc.first_section.body.paragraphs))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

