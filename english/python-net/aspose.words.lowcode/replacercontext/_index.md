---
title: ReplacerContext class
linktitle: ReplacerContext class
articleTitle: ReplacerContext class
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.ReplacerContext class. Find/replace operation context."
type: docs
weight: 150
url: /python-net/aspose.words.lowcode/replacercontext/
---

## ReplacerContext class

Find/replace operation context.


**Inheritance:** [ReplacerContext](./) → [ProcessorContext](../processorcontext/)

### Constructors
| Name | Description |
| --- | --- |
| [ReplacerContext()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [find_replace_options](./find_replace_options/) | Find/replace options. |
| [font_settings](../processorcontext/font_settings/) | Font settings used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [layout_options](../processorcontext/layout_options/) | Document layout options used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |
| [warning_callback](../processorcontext/warning_callback/) | Warning callback used by the processor.<br>(Inherited from [ProcessorContext](../processorcontext/)) |

### Methods

| Name | Description |
| --- | --- |
|[ set_replacement(pattern, replacement)](./set_replacement/#str_str) | Sets pattern and replacement used by find/replace operation. |
|[ set_replacement_regex(pattern, replacement)](./set_replacement_regex/#str_str) | Sets pattern and replacement used by find/replace operation. |

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

Shows how to replace string with regex in the document using context.

```python
# There is a several ways to replace string with regex in the document:
doc = MY_DIR + 'Footer.docx'
pattern = 'gr(a|e)y'
replacement = 'lavender'
replacer_context = aw.lowcode.ReplacerContext()
replacer_context.set_replacement_regex(pattern=pattern, replacement=replacement)
replacer_context.find_replace_options.find_whole_words_only = False
aw.lowcode.Replacer.create(replacer_context).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ReplaceContextRegex.docx').execute()
```

Shows how to replace string with regex in the document using documents from the stream using context.

```python
# There is a several ways to replace string with regex in the document using documents from the stream:
pattern = 'gr(a|e)y'
replacement = 'lavender'
with system_helper.io.FileStream(MY_DIR + 'Replace regex.docx', system_helper.io.FileMode.OPEN, system_helper.io.FileAccess.READ) as stream_in:
    replacer_context = aw.lowcode.ReplacerContext()
    replacer_context.set_replacement_regex(pattern=pattern, replacement=replacement)
    replacer_context.find_replace_options.find_whole_words_only = False
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'LowCode.ReplaceContextStreamRegex.docx', system_helper.io.FileMode.CREATE, system_helper.io.FileAccess.READ_WRITE) as stream_out:
        aw.lowcode.Replacer.create(replacer_context).from_stream(input=stream_in).to_stream(output=stream_out, save_format=aw.SaveFormat.DOCX).execute()
```

### See Also

* module [aspose.words.lowcode](../)
* class [ProcessorContext](../processorcontext/)

