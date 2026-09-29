---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /ru/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
---

## HtmlSaveOptions.font_resources_subsetting_size_threshold property

Controls which font resources need subsetting when saving to HTML, MHTML or EPUB.
Default is ``0``.



```python
@property
def font_resources_subsetting_size_threshold(self) -> int:
    ...

@font_resources_subsetting_size_threshold.setter
def font_resources_subsetting_size_threshold(self, value: int):
    ...

```

### Remarks

[HtmlSaveOptions.export_font_resources](../export_font_resources/) allows exporting fonts as subsidiary files or as parts of the output
package. If the document uses many fonts, especially with large number of glyphs, then output size can grow
significantly. Font subsetting reduces the size of the exported font resource by filtering out glyphs that
are not used by the current document.

Font subsetting works as follows:


* By default, all exported fonts are subsetted.
  
* Setting [HtmlSaveOptions.font_resources_subsetting_size_threshold](./) to a positive value
  instructs Aspose.Words to subset fonts which file size is larger than the specified value.
  
* Setting the property to int.MaxValue C# constant
  suppresses font subsetting.
  
**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





### Examples

Shows how to work with font subsetting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('Hello world!')
# При сохранении документа в HTML мы можем передать объект SaveOptions, чтобы настроить подмножество шрифтов.
# Предположим, мы установим флаг "export_font_resources" в "True" и также укажем папку в свойстве "fonts_folder".
# В этом случае операция сохранения создаст эту папку и поместит в неё файл .ttf
# для каждой шрифтовой гарнитуры, используемой нашим документом.
# Каждый файл .ttf будет содержать полный набор глифов этого шрифта,
# что может привести к получению очень большого файла, сопровождающего документ.
# Когда мы применяем подмножество к шрифту, его экспортированные необработанные данные будут содержать только глифы, которые документ
# использует вместо полного набора глифов. Если текст в нашем документе использует лишь небольшую часть набора глифов шрифта
# набор глифов, то подмножество значительно уменьшит размер наших выходных документов.
# Мы можем использовать свойство "font_resources_subsetting_size_threshold", чтобы задать размер файла .ttf в байтах.
# Если экспортированный шрифт создаёт файл большего размера, чем указано, то операция сохранения применит подмножество к этому шрифту.
# Установка порога 0 применяет подмножество ко всем шрифтам,
# а установка его в значение "2**31 - 1" фактически отключает подмножество.
fonts_folder = ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.fonts'
if os.path.exists(fonts_folder):
    shutil.rmtree(fonts_folder)
options = aw.saving.HtmlSaveOptions()
options.export_font_resources = True
options.fonts_folder = fonts_folder
options.font_resources_subsetting_size_threshold = font_resources_subsetting_size_threshold
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.font_subsetting.html', options)
font_file_names = glob.glob(fonts_folder + '/*.ttf')
self.assertEqual(3, len(font_file_names))
for filename in font_file_names:
    # По умолчанию файлы .ttf для каждого из наших трёх шрифтов будут превышать 700 МБ.
    # Подмножество уменьшит их все до менее чем 30 МБ.
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

