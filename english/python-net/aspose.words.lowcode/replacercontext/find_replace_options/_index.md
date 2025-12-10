---
title: ReplacerContext.find_replace_options property
linktitle: find_replace_options property
articleTitle: find_replace_options property
second_title: Aspose.Words for Python
description: "ReplacerContext.find_replace_options property. Find/replace options."
type: docs
weight: 20
url: /python-net/aspose.words.lowcode/replacercontext/find_replace_options/
---

## ReplacerContext.find_replace_options property

Find/replace options.


```python
@property
def find_replace_options(self) -> aspose.words.replacing.FindReplaceOptions:
    ...

```

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

* module [aspose.words.lowcode](../../)
* class [ReplacerContext](../)

