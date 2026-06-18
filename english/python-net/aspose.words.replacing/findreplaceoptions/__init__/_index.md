---
title: FindReplaceOptions constructor
linktitle: FindReplaceOptions constructor
articleTitle: FindReplaceOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.replacing.FindReplaceOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.replacing/findreplaceoptions/__init__/
---

## FindReplaceOptions() {#default}

Initializes a new instance of the FindReplaceOptions class with default settings.


```python
def __init__(self):
    ...
```

## FindReplaceOptions(direction) {#findreplacedirection}

Initializes a new instance of the FindReplaceOptions class with the specified direction.


```python
def __init__(self, direction: aspose.words.replacing.FindReplaceDirection):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| direction | [FindReplaceDirection](../../findreplacedirection/) | The direction of the find and replace operation. |

## FindReplaceOptions(replacing_callback) {#ireplacingcallback}

Initializes a new instance of the FindReplaceOptions class with the specified replacing callback.


```python
def __init__(self, replacing_callback: aspose.words.replacing.IReplacingCallback):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| replacing_callback | [IReplacingCallback](../../ireplacingcallback/) | The callback to use for replacing found text. |

## FindReplaceOptions(direction, replacing_callback) {#findreplacedirection_ireplacingcallback}

Initializes a new instance of the FindReplaceOptions class with the specified direction and replacing callback.


```python
def __init__(self, direction: aspose.words.replacing.FindReplaceDirection, replacing_callback: aspose.words.replacing.IReplacingCallback):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| direction | [FindReplaceDirection](../../findreplacedirection/) | The direction of the find and replace operation. |
| replacing_callback | [IReplacingCallback](../../ireplacingcallback/) | The callback to use for replacing found text. |

## Examples

Shows how to recognize and use substitutions within replacement patterns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Jason gave money to Paul.')
regex = '([A-z]+) gave money to ([A-z]+)'
options = aw.replacing.FindReplaceOptions()
options.use_substitutions = True
# Using legacy mode does not support many advanced features, so we need to set it to 'false'.
options.legacy_mode = False
doc.range.replace_regex(pattern=regex, replacement='$2 took money from $1', options=options)
self.assertEqual(doc.get_text(), 'Paul took money from Jason.\x0c')
```

Shows how to track the order in which a text replacement operation traverses nodes.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
first_page_section = doc.first_section
logger = self.ReplaceLog()
options = aw.replacing.FindReplaceOptions(replacing_callback=logger)
# Using a different header/footer for the first page will affect the search order.
first_page_section.page_setup.different_first_page_header_footer = different_first_page_header_footer
doc.range.replace_regex(pattern='(header|footer)', replacement='', options=options)
if different_first_page_header_footer:
    self.assertEqual('First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n', logger.text.replace('\r', ''))
else:
    self.assertEqual('Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n', logger.text.replace('\r', ''))
```

Shows how to track the order in which a text replacement operation traverses nodes (ReplaceLog).

```python
class ReplaceLog(aw.replacing.IReplacingCallback):

    @property
    def text(self):
        return str.join('', self.m_text_builder)

    def __init__(self):
        self.m_text_builder = []

    def replacing(self, args):
        self.m_text_builder.append(args.match_node.get_text() + '\n')
        return aw.replacing.ReplaceAction.SKIP
```

## See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

