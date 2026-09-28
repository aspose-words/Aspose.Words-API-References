---
title: HtmlSaveOptions.navigation_map_level property
linktitle: navigation_map_level property
articleTitle: navigation_map_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.navigation_map_level property. Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats"
type: docs
weight: 390
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/navigation_map_level/
---

## HtmlSaveOptions.navigation_map_level property

Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3
formats. Default value is ``3``.



```python
@property
def navigation_map_level(self) -> int:
    ...

@navigation_map_level.setter
def navigation_map_level(self, value: int):
    ...

```

### Remarks

The navigation map allows user agents to provide an easy way of navigation through the document structure.
Usually navigation points correspond to headings in the document. In order to populate headings up to level **N**
assign this value to [HtmlSaveOptions.navigation_map_level](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2**
and **Heading 3**.
You can set this property to a value from 1 to 9 in order to request the corresponding maximum level.
Setting it to zero will reduce the navigation map to only the document root or roots of document parts.




### Examples

Shows how to generate table of contents for Azw3 documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.AZW3)
options.navigation_map_level = 2
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.CreateAZW3Toc.azw3', save_options=options)
```

Shows how to generate table of contents for Mobi documents.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.MOBI)
options.navigation_map_level = 5
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.CreateMobiToc.mobi', save_options=options)
```

Shows how to filter headings that appear in the navigation panel of a saved Epub document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 我们使用 "Heading" 样式格式化的每个段落都可以作为标题。
# 每个标题还可能有一个标题级别，由其标题样式的数量决定。
# 以下标题的级别为 1-3。
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #1')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #2')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #3')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 1')
builder.writeln('Heading #4')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 2')
builder.writeln('Heading #5')
builder.paragraph_format.style = builder.document.styles.get_by_name('Heading 3')
builder.writeln('Heading #6')
# Epub 阅读器通常会为其文档创建目录。
# 文档中每个使用 "Heading" 样式的段落都会在此目录中生成一个条目。
# 我们可以使用 "NavigationMapLevel" 属性来设置最大标题级别。
# Epub 阅读器不会将级别高于我们指定的标题添加到目录中。
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.EPUB)
options.navigation_map_level = 2
# 我们的文档有六个标题，其中两个的级别高于 2。
# 此文档的目录将包含四个条目。
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.EpubHeadings.epub', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

