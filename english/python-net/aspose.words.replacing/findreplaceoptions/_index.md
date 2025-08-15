---
title: FindReplaceOptions class
linktitle: FindReplaceOptions class
articleTitle: FindReplaceOptions class
second_title: Aspose.Words for Python
description: "aspose.words.replacing.FindReplaceOptions class. Specifies options for find/replace operations"
type: docs
weight: 20
url: /python-net/aspose.words.replacing/findreplaceoptions/
---

## FindReplaceOptions class

Specifies options for find/replace operations.
To learn more, visit the [Find and Replace](https://docs.aspose.com/words/python-net/find-and-replace/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [FindReplaceOptions()](./__init__/#default) | Initializes a new instance of the FindReplaceOptions class with default settings. |
| [FindReplaceOptions(direction)](./__init__/#findreplacedirection) | Initializes a new instance of the FindReplaceOptions class with the specified direction. |
| [FindReplaceOptions(replacing_callback)](./__init__/#ireplacingcallback) | Initializes a new instance of the FindReplaceOptions class with the specified replacing callback. |
| [FindReplaceOptions(direction, replacing_callback)](./__init__/#findreplacedirection_ireplacingcallback) | Initializes a new instance of the FindReplaceOptions class with the specified direction and replacing callback. |

### Properties

| Name | Description |
| --- | --- |
| [apply_font](./apply_font/) | Text formatting applied to new content. |
| [apply_paragraph_format](./apply_paragraph_format/) | Paragraph formatting applied to new content. |
| [direction](./direction/) | Selects direction for replace. Default value is [FindReplaceDirection.FORWARD](../findreplacedirection/#FORWARD). |
| [find_whole_words_only](./find_whole_words_only/) | True indicates the oldValue must be a standalone word. |
| [ignore_deleted](./ignore_deleted/) | Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is ``False``. |
| [ignore_field_codes](./ignore_field_codes/) | Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is ``False``. |
| [ignore_fields](./ignore_fields/) | Gets or sets a boolean value indicating either to ignore text inside fields. The default value is ``False``. |
| [ignore_footnotes](./ignore_footnotes/) | Gets or sets a boolean value indicating either to ignore footnotes. The default value is ``False``. |
| [ignore_inserted](./ignore_inserted/) | Gets or sets a boolean value indicating either to ignore text inside insert revisions. The default value is ``False``. |
| [ignore_office_math](./ignore_office_math/) | Gets or sets a boolean value indicating either to ignore text inside OfficeMath/\>. The default value is ``True``. |
| [ignore_shapes](./ignore_shapes/) | Gets or sets a boolean value indicating either to ignore shapes within a text. |
| [ignore_structured_document_tags](./ignore_structured_document_tags/) | Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). The default value is ``False``. |
| [legacy_mode](./legacy_mode/) | Gets or sets a boolean value indicating that old find/replace algorithm is used. |
| [match_case](./match_case/) | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [replacement_format](./replacement_format/) | Specifies format of the replacement. Default is [ReplacementFormat.TEXT](../replacementformat/#TEXT). |
| [replacing_callback](./replacing_callback/) | The user-defined method which is called before every replace occurrence. |
| [smart_paragraph_break_replacement](./smart_paragraph_break_replacement/) | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. |
| [use_legacy_order](./use_legacy_order/) | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is ``False``. |
| [use_substitutions](./use_substitutions/) | Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is ``False``. |

### Examples

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Ruby bought a ruby necklace.')
# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()
# Set the "match_case" flag to "True" to apply case sensitivity while finding strings to replace.
# Set the "match_case" flag to "False" to ignore character case while searching for text to replace.
options.match_case = match_case
doc.range.replace('Ruby', 'Jade', options)
self.assertEqual('Jade bought a ruby necklace.' if match_case else 'Jade bought a Jade necklace.', doc.get_text().strip())
```

Shows how to toggle standalone word-only find-and-replace operations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Jackson will meet you in Jacksonville.')
# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()
# Set the "find_whole_words_only" flag to "True" to replace the found text if it is not a part of another word.
# Set the "find_whole_words_only" flag to "False" to replace all text regardless of its surroundings.
options.find_whole_words_only = find_whole_words_only
doc.range.replace('Jackson', 'Louis', options)
self.assertEqual('Louis will meet you in Jacksonville.' if find_whole_words_only else 'Louis will meet you in Louisville.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../)

