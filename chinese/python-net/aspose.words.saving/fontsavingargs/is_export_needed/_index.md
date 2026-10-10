---
title: FontSavingArgs.is_export_needed property
linktitle: is_export_needed property
articleTitle: is_export_needed property
second_title: Aspose.Words for Python
description: "FontSavingArgs.is_export_needed property. Allows to specify whether the current font will be exported as a font resource"
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/fontsavingargs/is_export_needed/
---

## FontSavingArgs.is_export_needed property

Allows to specify whether the current font will be exported as a font resource. Default is ``True``.



```python
@property
def is_export_needed(self) -> bool:
    ...

@is_export_needed.setter
def is_export_needed(self, value: bool):
    ...

```

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```python
def handle_font_saving(self, args):
    # 自定义逻辑：将字体导出到 ARTIFACTS_DIR 中的文件
    # args 是 FontSavingArgs
    if args.is_export_needed:
        font_file_name = args.font_file_name
        if not font_file_name:
            font_file_name = args.font_family_name + '.ttf'
        font_path = Path(ARTIFACTS_DIR) / font_file_name
        with open(font_path, 'wb') as f:
            # args.font_stream 是一个流对象（类似 io.BytesIO）
            f.write(args.font_stream.read())
        # 可选：如果以后需要，args.keep_font_stream_open = True
        args.keep_font_stream_open = False

def export_fonts_to_separate_files(self):
    doc = aw.Document(MY_DIR + 'Rendering.docx')
    options = aw.saving.HtmlSaveOptions()
    options.export_font_resources = True
    options.font_saving_callback = self.handle_font_saving
    # 回调将导出 .ttf 文件并将其保存到输出文档旁边。
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
        # 我们也可以从这里访问源文档。
        self.assertTrue(args.document.original_file_name.endswith('Rendering.docx'))
        self.assertTrue(args.is_export_needed)
        self.assertTrue(args.is_subsetting_needed)
        # 保存导出字体有两种方式。
        # 1 -  保存到本地文件系统位置：
        args.font_file_name = Path(args.original_file_name).name
        # 2 -  保存到流中：
        args.font_stream = open(Path(ARTIFACTS_DIR) / Path(args.original_file_name).name, 'wb')
        self.assertFalse(args.keep_font_stream_open)
```

### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)

