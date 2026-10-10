---
title: FontSavingArgs.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "FontSavingArgs.document property. Gets the document object that is being saved."
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/fontsavingargs/document/
---

## FontSavingArgs.document property

Gets the document object that is being saved.


```python
@property
def document(self) -> aspose.words.Document:
    ...

```

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # Anpassad logik: exportera teckensnitt till fil i ARTIFACTS_DIR
    # args är FontSavingArgs
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream är ett strömobjekt (liknande io.BytesIO)
            f.write(args.font_stream.read())
        # Valfritt: args.keep_font_stream_open = True om det behövs senare
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # Återanropet kommer att exportera .ttf-filer och spara dem tillsammans med det genererade dokumentet.
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
        # Vi kan också komma åt källdokumentet härifrån.
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # Det finns två sätt att spara ett exporterat teckensnitt.
        # 1 -  Spara det till en lokal filsystemplats:
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  Spara det till en ström:
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)

