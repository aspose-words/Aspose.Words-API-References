---
title: BuiltInDocumentProperties.lines property
linktitle: lines property
articleTitle: lines property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.lines property. Represents an estimate of the number of lines in the document."
type: docs
weight: 190
url: /python-net/aspose.words.properties/builtindocumentproperties/lines/
---

## BuiltInDocumentProperties.lines property

Represents an estimate of the number of lines in the document.


```python
@property
def lines(self) -> int:
    ...

@lines.setter
def lines(self, value: int):
    ...

```

### Remarks

Aspose.Words updates this property when you call [Document.update_word_count()](../../../aspose.words/document/update_word_count/#bool).




### Examples

Shows how to update all list labels in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.write('Ut enim ad minim veniam, ' + 'quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Aspose.Words does not track document metrics like these in real time.
self.assertEqual(0, doc.built_in_document_properties.characters)
self.assertEqual(0, doc.built_in_document_properties.words)
self.assertEqual(1, doc.built_in_document_properties.paragraphs)
self.assertEqual(1, doc.built_in_document_properties.lines)
# To get accurate values for three of these properties, we will need to update them manually.
doc.update_word_count()
self.assertEqual(196, doc.built_in_document_properties.characters)
self.assertEqual(36, doc.built_in_document_properties.words)
self.assertEqual(2, doc.built_in_document_properties.paragraphs)
# For the line count, we will need to call a specific overload of the updating method.
self.assertEqual(1, doc.built_in_document_properties.lines)
doc.update_word_count(True)
self.assertEqual(4, doc.built_in_document_properties.lines)
```

Shows how to work with document properties in the "Content" category.

```python
def content_test():
    doc = aw.Document(MY_DIR + 'Paragraphs.docx')
    properties = doc.built_in_document_properties
    # By using built in properties,
    # we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
    # These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
    # If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
    # Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
    # Page count: The page_count property shows the page count in real time and its value can be assigned to the Pages property
    # The "pages" property stores the page count of the document.
    self.assertEqual(6, properties.pages)
    # The "words", "characters", and "characters_with_spaces" built-in properties also display various document statistics,
    # but we need to call the "update_word_count" method on the whole document before we can expect them to contain accurate values.
    doc.update_word_count()
    self.assertEqual(1035, properties.words)
    self.assertEqual(6026, properties.characters)
    self.assertEqual(7041, properties.characters_with_spaces)
    # Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
    line_counter = LineCounter(doc)
    properties.lines = line_counter.get_line_count()
    self.assertEqual(142, properties.lines)
    # Assign the number of Paragraph nodes in the document to the "paragraphs" built-in property.
    properties.paragraphs = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True).count
    self.assertEqual(29, properties.paragraphs)
    # Get an estimate of the file size of our document via the "bytes" built-in property.
    self.assertEqual(20310, properties.bytes)
    # Set a different template for our document, and then update the "template" built-in property manually to reflect this change.
    doc.attached_template = MY_DIR + 'Business brochure.dotx'
    self.assertEqual('Normal', properties.template)
    properties.template = doc.attached_template
    # "content_status" is a descriptive built-in property.
    properties.content_status = 'Draft'
    # Upon saving, the "content_type" built-in property will contain the MIME type of the output save format.
    self.assertEqual('', properties.content_type)
    # If the document contains links, and they are all up to date, we can set the "links_up_to_date" property to "True".
    self.assertFalse(properties.links_up_to_date)
    doc.save(ARTIFACTS_DIR + 'DocumentProperties.content.docx')

class LineCounter:
    """Counts the lines in a document.
    Traverses the document's layout entities tree upon construction,
    counting entities of the "Line" type that also contain real text."""

    def __init__(self, doc: aw.Document):
        self.layout_enumerator = aw.layout.LayoutEnumerator(doc)
        self.line_count = 0
        self.scanning_line_for_real_text = False
        self.count_lines()

    def get_line_count(self) -> int:
        return self.line_count

    def count_lines(self) -> int:
        while True:
            if self.layout_enumerator.type == aw.layout.LayoutEntityType.LINE:
                self.scanning_line_for_real_text = True
            if self.layout_enumerator.move_first_child():
                if self.scanning_line_for_real_text and self.layout_enumerator.kind.startswith('TEXT'):
                    self.line_count += 1
                    self.scanning_line_for_real_text = False
                self.count_lines()
                self.layout_enumerator.move_parent()
            if not self.layout_enumerator.move_next():
                break
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

