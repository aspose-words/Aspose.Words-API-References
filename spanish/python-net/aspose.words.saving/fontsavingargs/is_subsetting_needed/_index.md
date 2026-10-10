---
title: FontSavingArgs.is_subsetting_needed property
linktitle: is_subsetting_needed property
articleTitle: is_subsetting_needed property
second_title: Aspose.Words for Python
description: "FontSavingArgs.is_subsetting_needed property. Allows to specify whether the current font will be subsetted before exporting as a font resource."
type: docs
weight: 70
url: /es/python-net/aspose.words.saving/fontsavingargs/is_subsetting_needed/
---

## FontSavingArgs.is_subsetting_needed property

Allows to specify whether the current font will be subsetted before exporting as a font resource.


```python
@property
def is_subsetting_needed(self) -> bool:
    ...

@is_subsetting_needed.setter
def is_subsetting_needed(self, value: bool):
    ...

```

### Remarks

Fonts can be exported as complete original font files or subsetted to include only the characters
that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size 
with the one specified in [HtmlSaveOptions.font_resources_subsetting_size_threshold](../../htmlsaveoptions/font_resources_subsetting_size_threshold/). 
You can override this behavior for individual fonts by setting the [FontSavingArgs.is_subsetting_needed](./) property.




### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # Lógica personalizada: exportar la fuente a un archivo en ARTIFACTS_DIR
    # args es FontSavingArgs
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream es un objeto de flujo (similar a io.BytesIO)
            f.write(args.font_stream.read())
        # Opcional: args.keep_font_stream_open = True si se necesita más tarde
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # La devolución de llamada exportará archivos .ttf y los guardará junto al documento de salida.
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
        # También podemos acceder al documento fuente desde aquí.
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # Hay dos formas de guardar una fuente exportada.
        # 1 -  Guardarla en una ubicación del sistema de archivos local:
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  Guardarla en un flujo:
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)

