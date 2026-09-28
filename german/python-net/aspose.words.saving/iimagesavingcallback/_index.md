---
title: IImageSavingCallback class
linktitle: IImageSavingCallback class
articleTitle: IImageSavingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.saving.IImageSavingCallback class. Implement this interface if you want to control how Aspose.Words saves images when  saving a document to HTML"
type: docs
weight: 340
url: /de/python-net/aspose.words.saving/iimagesavingcallback/
---

## IImageSavingCallback class

Implement this interface if you want to control how Aspose.Words saves images when 
saving a document to HTML. May be used by other formats.


### Methods

| Name | Description |
| --- | --- |
|[ image_saving(args)](./image_saving/#imagesavingargs) | Called when Aspose.Words saves an image to HTML. |

### Examples

Shows how to rename the image name during saving into Markdown document.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
save_options = aw.saving.MarkdownSaveOptions()
# Wenn wir ein Dokument, das Bilder enthält, in Markdown konvertieren, erhalten wir eine Markdown‑Datei, die auf mehrere Bilder verweist.
# Jedes Bild wird als Datei im lokalen Dateisystem vorliegen.
# Es gibt außerdem einen Callback, der den Namen und den Speicherort jeder Bilddatei im Dateisystem anpassen kann.
save_options.image_saving_callback = self.SavedImageRename('MarkdownSaveOptions.HandleDocument.md')
save_options.save_format = aw.SaveFormat.MARKDOWN
# Die Methode ImageSaving() unseres Callbacks wird zu diesem Zeitpunkt ausgeführt.
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

* module [aspose.words.saving](../)

