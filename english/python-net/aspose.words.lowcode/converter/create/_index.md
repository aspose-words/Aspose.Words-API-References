---
title: Converter.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "aspose.words.lowcode.Converter.create method"
type: docs
weight: 30
url: /python-net/aspose.words.lowcode/converter/create/
---

## create() {#default}

Creates new instance of the converter processor.


```python
def create(self):
    ...
```

## create(context) {#convertercontext}

Creates new instance of the converter processor.


```python
def create(self, context: aspose.words.lowcode.ConverterContext):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| context | [ConverterContext](../../convertercontext/) |  |

## Examples

Shows how to convert documents with a single line of code using context.

```python
doc = MY_DIR + 'Big document.docx'
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.1.pdf').execute()
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.2.pdf', save_format=aw.SaveFormat.RTF).execute()
save_options = aw.saving.OoxmlSaveOptions()
save_options.password = 'Aspose.Words'
load_options = aw.loading.LoadOptions()
load_options.ignore_ole_data = True
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc, load_options=load_options).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.3.docx', save_options=save_options).execute()
aw.lowcode.Converter.create(aw.lowcode.ConverterContext()).from_file(input=doc).to_file(output=ARTIFACTS_DIR + 'LowCode.ConvertContext.4.png', save_options=aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)).execute()
```

## See Also

* module [aspose.words.lowcode](../../)
* class [Converter](../)

