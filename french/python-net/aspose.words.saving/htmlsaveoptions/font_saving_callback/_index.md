---
title: HtmlSaveOptions.font_saving_callback property
linktitle: font_saving_callback property
articleTitle: font_saving_callback property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_saving_callback property. Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB."
type: docs
weight: 300
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/font_saving_callback/
---

## HtmlSaveOptions.font_saving_callback property

Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB.


```python
@property
def font_saving_callback(self) -> aspose.words.saving.IFontSavingCallback:
    ...

@font_saving_callback.setter
def font_saving_callback(self, value: aspose.words.saving.IFontSavingCallback):
    ...

```

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # Logique personnalisée : exporter la police vers un fichier dans ARTIFACTS_DIR
    # args est FontSavingArgs
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream est un objet flux (type io.BytesIO)
            f.write(args.font_stream.read())
        # Optionnel : args.keep_font_stream_open = True si besoin ultérieur
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # Le rappel exportera les fichiers .ttf et les enregistrera à côté du document de sortie.
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
        # Nous pouvons également accéder au document source depuis ici.
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # Il existe deux manières d'enregistrer une police exportée.
        # 1 -  Enregistrez-la à un emplacement du système de fichiers local :
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  Enregistrez-la dans un flux :
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

