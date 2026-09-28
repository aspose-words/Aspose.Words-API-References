---
title: PageSet constructor
linktitle: PageSet constructor
articleTitle: PageSet constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet constructor"
type: docs
weight: 10
url: /zh/python-net/aspose.words.saving/pageset/__init__/
---

## PageSet(page) {#int}

Creates an one-page set based on exact page index.


```python
def __init__(self, page: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| page | int | Zero-based index of the page. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(pages) {#intlist}

Creates a page set based on exact page indices.


```python
def __init__(self, pages: List[int]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pages | List[int] | Zero-based indices of pages. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(ranges) {#pagerangelist}

Creates a page set based on ranges.


```python
def __init__(self, ranges: List[aspose.words.saving.PageRange]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ranges | List[[PageRange](../../pagerange/)] | Array of page ranges. |

### Remarks

If a range is encountered that starts after the last page in the document, 
an exception will be thrown during rendering.
All ranges that end after the last page are truncated to fit in the document.


## Examples

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# 创建一个 "ImageSaveOptions" 对象，以便我们传递给文档的 "Save" 方法
# 以修改该方法将文档渲染为图像的方式。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# 将 "PageSet" 设置为 "1" 以选择第二页，通过
# 从零基索引开始渲染文档。
options.page_set = aw.saving.PageSet(page=1)
# 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
# 此图像将包含从第二页开始的单页，
# 这将仅是原始文档的第二页。
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 向文档添加五页。
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# 创建一个 "XpsSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改该方法将文档转换为 .XPS 的方式。
xps_options = aw.saving.XpsSaveOptions()
# 使用 "PageSet" 属性选择文档的一组页面，以保存为输出 XPS。
# 在这种情况下，我们将通过零基索引仅选择三页：第 1 页、第 2 页和第 4 页。
xps_options.page_set = aw.saving.PageSet(pages=[0, 1, 3])
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.ExportExactPages.xps', save_options=xps_options)
```

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
page_set = aw.saving.PageSet(ranges=[aw.saving.PageRange(1, 1), aw.saving.PageRange(2, 3), aw.saving.PageRange(1, 3), aw.saving.PageRange(2, 4), aw.saving.PageRange(1, 1)])
image_options.page_set = page_set
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ExportVariousPageRanges.tiff', save_options=image_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

