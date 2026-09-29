---
title: MarkdownSaveOptions.image_saving_callback property
linktitle: image_saving_callback property
articleTitle: image_saving_callback property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.image_saving_callback property. Allows to control how images are saved when a document is saved to [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format."
type: docs
weight: 70
url: /sv/python-net/aspose.words.saving/markdownsaveoptions/image_saving_callback/
---

## MarkdownSaveOptions.image_saving_callback property

Allows to control how images are saved when a document is saved to
[SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format.



```python
@property
def image_saving_callback(self) -> aspose.words.saving.IImageSavingCallback:
    ...

@image_saving_callback.setter
def image_saving_callback(self, value: aspose.words.saving.IImageSavingCallback):
    ...

```

### Examples

Shows how to rename the image name during saving into Markdown document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.MarkdownSaveOptions()
# Om vi konverterar ett dokument som innehåller bilder till Markdown får vi en Markdown‑fil som länkar till flera bilder.
# Varje bild kommer att vara i form av en fil i det lokala filsystemet.
# Det finns också en återuppringning som kan anpassa namnet och filsystemplatsen för varje bild.
save_options.image_saving_callback = self.SavedImageRename('MarkdownSaveOptions.HandleDocument.md')
save_options.save_format = aw.SaveFormat.MARKDOWN
# Metoden ImageSaving() i vår återuppringning kommer att köras vid detta tillfälle.
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

