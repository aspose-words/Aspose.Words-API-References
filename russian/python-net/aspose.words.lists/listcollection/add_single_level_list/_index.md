---
title: ListCollection.add_single_level_list method
linktitle: add_single_level_list method
articleTitle: add_single_level_list method
second_title: Aspose.Words for Python
description: "ListCollection.add_single_level_list method. Creates a new single level list based on the predefined template and adds it to the list collection in the document."
type: docs
weight: 60
url: /ru/python-net/aspose.words.lists/listcollection/add_single_level_list/
---

## add_single_level_list(list_template) {#listtemplate}

Creates a new single level list based on the predefined template and adds it to the list collection in the document.


```python
def add_single_level_list(self, list_template: aspose.words.lists.ListTemplate):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| list_template | [ListTemplate](../../listtemplate/) |  |

### Examples

Shows how to create a new single level list based on the predefined template.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
list_collection = doc.lists
# Создаёт маркированный список из шаблона BulletCircle.
bulleted_list = list_collection.add_single_level_list(aw.lists.ListTemplate.BULLET_CIRCLE)
# Записывает маркированный список в полученный документ.
builder.writeln('Bulleted list starts below:')
builder.list_format.list = bulleted_list
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# Создаёт нумерованный список из шаблона NumberUppercaseLetterDot.
numbered_list = list_collection.add_single_level_list(aw.lists.ListTemplate.NUMBER_UPPERCASE_LETTER_DOT)
# Записывает нумерованный список в полученный документ.
builder.writeln('Numbered list starts below:')
builder.list_format.list = numbered_list
builder.writeln('Item 1')
builder.writeln('Item 2')
doc.save(file_name=ARTIFACTS_DIR + 'Lists.AddSingleLevelList.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListCollection](../)

