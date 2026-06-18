---
title: FontSavingArgs.font_file_name property
linktitle: font_file_name property
articleTitle: font_file_name property
second_title: Aspose.Words for Python
description: "FontSavingArgs.font_file_name property. Gets or sets the file name (without path) where the font will be saved to."
type: docs
weight: 40
url: /python-net/aspose.words.saving/fontsavingargs/font_file_name/
---

## FontSavingArgs.font_file_name property

Gets or sets the file name (without path) where the font will be saved to.


```python
@property
def font_file_name(self) -> str:
    ...

@font_file_name.setter
def font_file_name(self, value: str):
    ...

```

### Remarks

This property allows you to redefine how the font file names are generated
during export to HTML.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the font into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded font when 
exporting to HTML format. How the font file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated font file name looks like 
*\<document base file name\>.\<original file name\>\<optional suffix\>.\<extension\>*.

When saving a document to a stream, the generated font file name looks like 
*Aspose.Words.\<document guid\>.\<original file name\>\<optional suffix\>.\<extension\>*.

[FontSavingArgs.font_file_name](./) must contain only the file name without the path.
Aspose.Words determines the path for saving using the document file name, 
the [HtmlSaveOptions.fonts_folder](../../htmlsaveoptions/fonts_folder/) and
[HtmlSaveOptions.fonts_folder_alias](../../htmlsaveoptions/fonts_folder_alias/) properties.




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

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)
* property [FontSavingArgs.font_stream](../font_stream/)
* property [HtmlSaveOptions.fonts_folder](../../htmlsaveoptions/fonts_folder/)
* property [HtmlSaveOptions.fonts_folder_alias](../../htmlsaveoptions/fonts_folder_alias/)

