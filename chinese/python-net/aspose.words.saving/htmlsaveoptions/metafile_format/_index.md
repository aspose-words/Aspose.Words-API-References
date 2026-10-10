---
title: HtmlSaveOptions.metafile_format property
linktitle: metafile_format property
articleTitle: metafile_format property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.metafile_format property. Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB"
type: docs
weight: 380
url: /zh/python-net/aspose.words.saving/htmlsaveoptions/metafile_format/
---

## HtmlSaveOptions.metafile_format property

Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB.
Default value is [HtmlMetafileFormat.PNG](../../htmlmetafileformat/#PNG), meaning that metafiles are rendered to raster PNG images.



```python
@property
def metafile_format(self) -> aspose.words.saving.HtmlMetafileFormat:
    ...

@metafile_format.setter
def metafile_format(self, value: aspose.words.saving.HtmlMetafileFormat):
    ...

```

### Remarks

Metafiles are not natively displayed by HTML browsers. By default, Aspose.Words converts WMF and EMF
images into PNG files when exporting to HTML. Other options are to convert metafiles to SVG images or to export
them as is without conversion.

Some image transforms, in particular image cropping, will not be applied to metafile images if they
are exported to HTML without conversion.




### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```python
html = "<html>\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\n                    </svg>\n                </html>"
# 使用 'ConvertSvgToEmf' 恢复旧行为
# 其中所有从 HTML 文档加载的 SVG 图像都会被转换为 EMF。
# 现在 SVG 图像加载时不再进行转换
# 如果加载选项中指定的 MS Word 版本本地支持 SVG 图像。
load_options = aw.loading.HtmlLoadOptions()
load_options.convert_svg_to_emf = True
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=load_options)
# 此文档包含以文本形式呈现的 <svg> 元素。
# 当我们将文档保存为 HTML 时，可以传入 SaveOptions 对象
# 以确定保存操作如何处理此对象。
# 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.Png" 以将其转换为 PNG 图像。
# 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.Svg" 以保持其为 SVG 对象。
# 将 "MetafileFormat" 属性设置为 "HtmlMetafileFormat.EmfOrWmf" 以将其转换为元文件。
options = aw.saving.HtmlSaveOptions()
options.metafile_format = html_metafile_format
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.MetafileFormat.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.MetafileFormat.html')
switch_condition = html_metafile_format
if switch_condition == aw.saving.HtmlMetafileFormat.PNG:
    self.assertTrue('<p style="margin-top:0pt; margin-bottom:0pt">' + '<img src="HtmlSaveOptions.MetafileFormat.001.png" width="500" height="40" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>' in out_doc_contents)
elif switch_condition == aw.saving.HtmlMetafileFormat.SVG:
    self.assertTrue('<span style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline">' + '<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="499" height="40">' in out_doc_contents)
elif switch_condition == aw.saving.HtmlMetafileFormat.EMF_OR_WMF:
    self.assertTrue('<p style="margin-top:0pt; margin-bottom:0pt">' + '<img src="HtmlSaveOptions.MetafileFormat.001.emf" width="500" height="40" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.image_resolution](../image_resolution/)
* property [HtmlSaveOptions.scale_image_to_shape_size](../scale_image_to_shape_size/)

