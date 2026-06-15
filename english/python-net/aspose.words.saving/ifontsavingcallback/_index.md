---
title: IFontSavingCallback class
linktitle: IFontSavingCallback class
articleTitle: IFontSavingCallback class
second_title: Aspose.Words for Python
description: "aspose.words.saving.IFontSavingCallback class. Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format."
type: docs
weight: 330
url: /python-net/aspose.words.saving/ifontsavingcallback/
---

## IFontSavingCallback class

Implement this interface if you want to receive notifications and control how
Aspose.Words saves fonts when exporting a document to HTML format.


### Methods

| Name | Description |
| --- | --- |
|[ font_saving(args)](./font_saving/#fontsavingargs) | Called when Aspose.Words is about to save a font resource. |

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # Custom logic: export font to file in ARTIFACTS_DIR
    # args is FontSavingArgs
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream is a stream object (io.BytesIO-like)
            f.write(args.font_stream.read())
        # Optional: args.keep_font_stream_open = True if needed later
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # The callback will export .ttf files and save them alongside the output document.
    doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.SaveExportedFonts.html', save_options=options)
    for font_filename in [str(f) for f in Path(ARTIFACTS_DIR).iterdir() if f.suffix == '.ttf']:
        print(font_filename)
```

Shows how to define custom logic for exporting fonts when saving to HTML (HandleFontSaving).

```python
class HandleFontSaving(aw.saving.IFontSavingCallback):

    def font_saving(self, args):
        from pathlib import Path
        from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
        print(f'Font:\t{args.font_family_name}')
        if args.bold:
            print(', bold')
        if args.italic:
            print(', italic')
        print(f'\nSource:\t{args.original_file_name}, {args.original_file_size} bytes\n')
        # We can also access the source document from here.
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # There are two ways of saving an exported font.
        # 1 -  Save it to a local file system location:
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  Save it to a stream:
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../)

