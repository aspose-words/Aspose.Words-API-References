---
title: ListCollection.add_copy method
linktitle: add_copy method
articleTitle: add_copy method
second_title: Aspose.Words for Python
description: "ListCollection.add_copy method. Creates a new list by copying the specified list and adding it to the collection of lists in the document."
type: docs
weight: 50
url: /python-net/aspose.words.lists/listcollection/add_copy/
---

## add_copy(src_list) {#list}

Creates a new list by copying the specified list and adding it to the collection of lists in the document.


```python
def add_copy(self, src_list: aspose.words.lists.List):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_list | [List](../../list/) | The source list to copy from. |

### Remarks

The source list can be from any document. If the source list belongs to a different document,
a copy of the list is created and added to the current document.

If the source list is a reference to or a definition of a list style,
the newly created list is not related to the original list style.




### Returns

The newly created list.


### Examples

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Create a list from a Microsoft Word template, and customize its first list level.
list1 = doc.lists.add(aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# Apply our list to some paragraphs.
builder = aw.DocumentBuilder(doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# We can add a copy of an existing list to the document's list collection
# to create a similar list without making changes to the original.
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# Apply the second list to new paragraphs.
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(ARTIFACTS_DIR + 'Lists.restart_numbering_using_list_copy.docx')
```

Shows how to create a document with a sample of all the lists from another document.

```python
def print_out_all_lists():
    src_doc = aw.Document(MY_DIR + 'Rendering.docx')
    dst_doc = aw.Document()
    builder = aw.DocumentBuilder(dst_doc)
    for src_list in src_doc.lists:
        dst_list = dst_doc.lists.add_copy(src_list)
        add_list_sample(builder, dst_list)
    dst_doc.save(ARTIFACTS_DIR + 'Lists.print_out_all_lists.docx')

def add_list_sample(builder: aw.DocumentBuilder, list: aw.lists.List):
    builder.writeln(f'Sample formatting of list with list_id: {list.list_id}')
    builder.list_format.list = list
    for i in range(list.list_levels.count):
        builder.list_format.list_level_number = i
        builder.writeln(f'Level {i}')
    builder.list_format.remove_numbers()
    builder.writeln()
```

### See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

