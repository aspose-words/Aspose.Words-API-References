---
title: HtmlSaveOptions.font_resources_subsetting_size_threshold property
linktitle: font_resources_subsetting_size_threshold property
articleTitle: font_resources_subsetting_size_threshold property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.font_resources_subsetting_size_threshold property. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB"
type: docs
weight: 290
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/font_resources_subsetting_size_threshold/
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
# 当我们将文档保存为 HTML 时，可以传入 SaveOptions 对象来配置字体子集化。
# 假设我们将 \"export_font_resources\" 标志设置为 \"True\"，并在 \"fonts_folder\" 属性中指定一个文件夹。
# 在这种情况下，保存操作将创建该文件夹并在其中放置 .ttf 文件
# 该文件夹中每个我们文档使用的字体对应一个文件。
# 每个 .ttf 文件将包含该字体的完整字形集，
# 这可能导致随文档一起的文件体积非常大。
# 当我们对字体应用子集化时，导出的原始数据将仅包含文档使用的字形
# 使用，而不是整个字形集。如果文档中的文本仅使用了字体的很小一部分
# 字形集，那么子集化将显著减小我们输出文档的大小。
# 我们可以使用 "font_resources_subsetting_size_threshold" 属性来定义 .ttf 文件的大小（单位为字节）。
# 如果导出的字体文件大小超过该阈值，则保存操作将对该字体应用子集化。
# 将阈值设置为 0 将对所有字体应用子集化，
# 将其设置为 "2**31 - 1" 则实际上禁用子集化。
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
    # 默认情况下，我们的三种字体的 .ttf 文件大小都将超过 700MB。
    # 子集化将把它们全部减至 30MB 以下。
    font_file_size = os.path.getsize(filename)
    self.assertTrue(font_file_size > 700000 or font_file_size < 30000)
    self.assertTrue(max(font_resources_subsetting_size_threshold, 30000) > font_file_size)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)

