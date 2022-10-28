---
title: export_generator_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "When ``True``, causes the name and version of Aspose.Words to be embedded into produced files"
type: docs
weight: 60
url: /python-net/aspose.words.saving/saveoptions/export_generator_name/
---

## SaveOptions.export_generator_name property

When ``True``, causes the name and version of Aspose.Words to be embedded into produced files.
Default value is ``True``.



### Examples

Shows how to disable adding name and version of Aspose.Words into produced files.

```python
doc = aw.Document()

# Use https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ to know how to check the result.
save_options = aw.saving.OoxmlSaveOptions()
save_options.export_generator_name = False

doc.save(ARTIFACTS_DIR + "OoxmlSaveOptions.export_generator_name.docx", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

