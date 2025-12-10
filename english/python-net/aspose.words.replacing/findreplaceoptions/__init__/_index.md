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

## See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

