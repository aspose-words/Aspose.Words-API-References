---
title: FontSavingArgs class
linktitle: FontSavingArgs class
articleTitle: FontSavingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.saving.FontSavingArgs class. Provides data for the [IFontSavingCallback.font_saving()](../ifontsavingcallback/font_saving/#fontsavingargs) event"
type: docs
weight: 210
url: /python-net/aspose.words.saving/fontsavingargs/
---

## FontSavingArgs class

Provides data for the [IFontSavingCallback.font_saving()](../ifontsavingcallback/font_saving/#fontsavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Remarks

When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.export_font_resources](../htmlsaveoptions/export_font_resources/) 
is set to ``True``, it saves each font subject for export into a separate file.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to 
completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [FontSavingArgs.is_export_needed](./is_export_needed/) property.

To save fonts into streams instead of files, use the [FontSavingArgs.font_stream](./font_stream/) property.




### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | Indicates whether the current font is bold. |
| [document](./document/) | Gets the document object that is being saved. |
| [font_family_name](./font_family_name/) | Indicates the current font family name. |
| [font_file_name](./font_file_name/) | Gets or sets the file name (without path) where the font will be saved to. |
| [font_stream](./font_stream/) | Allows to specify the stream where the font will be saved to. |
| [is_export_needed](./is_export_needed/) | Allows to specify whether the current font will be exported as a font resource. Default is ``True``. |
| [is_subsetting_needed](./is_subsetting_needed/) | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [italic](./italic/) | Indicates whether the current font is italic. |
| [keep_font_stream_open](./keep_font_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [original_file_name](./original_file_name/) | Gets the original font file name with an extension. |
| [original_file_size](./original_file_size/) | Gets the original font file size. |

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

