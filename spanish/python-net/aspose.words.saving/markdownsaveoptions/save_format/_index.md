---
title: MarkdownSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 140
url: /es/python-net/aspose.words.saving/markdownsaveoptions/save_format/
---

## MarkdownSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to rename the image name during saving into Markdown document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.MarkdownSaveOptions()
# Si convertimos un documento que contiene imágenes a Markdown, terminaremos con un archivo Markdown que enlaza a varias imágenes.
# Cada imagen estará en forma de un archivo en el sistema de archivos local.
# También hay una devolución de llamada que puede personalizar el nombre y la ubicación en el sistema de archivos de cada imagen.
save_options.image_saving_callback = self.SavedImageRename('MarkdownSaveOptions.HandleDocument.md')
save_options.save_format = aw.SaveFormat.MARKDOWN
# El método ImageSaving() de nuestra devolución de llamada se ejecutará en este momento.
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

