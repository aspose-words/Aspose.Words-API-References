---
title: FontSavingArgs.font_family_name property
linktitle: font_family_name property
articleTitle: font_family_name property
second_title: Aspose.Words for Python
description: "FontSavingArgs.font_family_name property. Indicates the current font family name."
type: docs
weight: 30
url: /tr/python-net/aspose.words.saving/fontsavingargs/font_family_name/
---

## FontSavingArgs.font_family_name property

Indicates the current font family name.


```python
@property
def font_family_name(self) -> str:
    ...

```

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # Özel mantık: yazı tipini ARTIFACTS_DIR içinde bir dosyaya dışa aktar
    # args, FontSavingArgs'tir
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream, bir akış nesnesidir (io.BytesIO benzeri)
            f.write(args.font_stream.read())
        # İsteğe bağlı: args.keep_font_stream_open = True, daha sonra gerekirse
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # Geri arama, .ttf dosyalarını dışa aktaracak ve çıktı belgesiyle birlikte kaydedecek.
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
        # Kaynak belgeye buradan da erişebiliriz.
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # Dışa aktarılan bir yazı tipini kaydetmenin iki yolu vardır.
        # 1 -  Yerel dosya sistemi konumuna kaydedin:
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  Bir akışa kaydedin:
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)

