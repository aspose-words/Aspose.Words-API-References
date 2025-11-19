---
title: ReplacerContext.set_replacement method
linktitle: set_replacement method
articleTitle: set_replacement method
second_title: Aspose.Words for Python
description: "ReplacerContext.set_replacement method. Sets pattern and replacement used by find/replace operation."
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/replacercontext/set_replacement/
---

## set_replacement(pattern, replacement) {#str_str}

Sets pattern and replacement used by find/replace operation.


```python
def set_replacement(self, pattern: str, replacement: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | str |  |
| replacement | str |  |

### Remarks

Using this method overrides previously set pattern and replacement.


### Examples

Shows how to replace string in the document using context.

```python
# There is a several ways to replace string in the document:
doc = MY_DIR + 'Footer.docx'
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
replacer_context = aw.lowcode.ReplacerContext()
replacer_context.set_replacement(pattern=pattern, replacement=replacement)
replacer_context.find_replace_options.find_whole_words_only = False
aw.lowcode.Replacer.create(replacer_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ReplaceContext.docx').execute()
```

Shows how to replace string in the document using documents from the stream using context.

```python
# There is a several ways to replace string in the document using documents from the stream:
pattern = '(C)2006 Aspose Pty Ltd.'
replacement = 'Copyright (C) 2024 by Aspose Pty Ltd.'
with system_helper.io.FileStream(MY_DIR + 'Footer.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    replacer_context = aw.lowcode.ReplacerContext()
    replacer_context.set_replacement(pattern=pattern, replacement=replacement)
    replacer_context.find_replace_options.find_whole_words_only = False
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ReplaceContextStream.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Replacer.create(replacer_context).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../../)
* class [ReplacerContext](../)

