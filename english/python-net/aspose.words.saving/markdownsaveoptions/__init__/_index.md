---
title: MarkdownSaveOptions constructor
linktitle: MarkdownSaveOptions constructor
articleTitle: MarkdownSaveOptions constructor
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format."
type: docs
weight: 10
url: /python-net/aspose.words.saving/markdownsaveoptions/__init__/
---

## MarkdownSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format.



```python
def __init__(self):
    ...
```

### Examples

Shows how to rename the image name during saving into Markdown document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.MarkdownSaveOptions()
# If we convert a document that contains images into Markdown, we will end up with one Markdown file which links to several images.
# Each image will be in the form of a file in the local file system.
# There is also a callback that can customize the name and file system location of each image.
save_options.image_saving_callback = self.SavedImageRename('MarkdownSaveOptions.HandleDocument.md')
save_options.save_format = aw.SaveFormat.MARKDOWN
# The ImageSaving() method of our callback will be run at this time.
doc.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.HandleDocument.md', save_options=save_options)
self.assertEqual(1, len(list(filter(lambda f: f.endswith('.jpeg'), list(filter(lambda s: s.startswith(ARTIFACTS_DIR + 'MarkdownSaveOptions.HandleDocument.md shape'), list(system_helper.io.Directory.get_files(ARTIFACTS_DIR))))))))
self.assertEqual(8, len(list(filter(lambda f: f.endswith('.png'), list(filter(lambda s: s.startswith(ARTIFACTS_DIR + 'MarkdownSaveOptions.HandleDocument.md shape'), list(system_helper.io.Directory.get_files(ARTIFACTS_DIR))))))))
```

Shows how to rename the image name during saving into Markdown document (SavedImageRename).

```python
class SavedImageRename(aw.saving.IImageSavingCallback):

    def __init__(self, out_file_name):
        self.m_out_file_name = out_file_name
        self.m_count = 0

    def image_saving(self, args):
        from pathlib import Path
        self.m_count += 1
        image_file_name = f'{self.m_out_file_name} shape {self.m_count}, of type {args.current_shape.shape_type}{Path(args.image_file_name).suffix}'
        args.image_file_name = image_file_name
        args.image_stream = system_helper.io.FileStream(ARTIFACTS_DIR + image_file_name, system_helper.io.FileMode.CREATE)
        assert args.is_image_available
        assert not args.keep_image_stream_open
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

