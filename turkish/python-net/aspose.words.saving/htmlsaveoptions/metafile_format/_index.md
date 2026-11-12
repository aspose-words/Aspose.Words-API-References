---
title: HtmlSaveOptions.metafile_format property
linktitle: metafile_format property
articleTitle: metafile_format property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.metafile_format property. Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB"
type: docs
weight: 380
url: /tr/python-net/aspose.words.saving/htmlsaveoptions/metafile_format/
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
# 'ConvertSvgToEmf' kullanarak eski davranışı geri getirin
# burada bir HTML belgesinden yüklenen tüm SVG görüntüleri EMF'ye dönüştürülürdü.
# Artık SVG görüntüleri dönüşüm olmadan yüklenir
# yükleme seçeneklerinde belirtilen MS Word sürümü SVG görüntülerini yerel olarak destekliyorsa.
load_options = aw.loading.HtmlLoadOptions()
load_options.convert_svg_to_emf = True
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=load_options)
# Bu belge, metin biçiminde bir <svg> öğesi içerir.
# Belgeyi HTML olarak kaydettiğimizde bir SaveOptions nesnesi geçebiliriz
# kaydetme işleminin bu nesneyi nasıl işlediğini belirlemek için.
# "MetafileFormat" özelliğini "HtmlMetafileFormat.Png" olarak ayarlayarak PNG görüntüsüne dönüştürmek.
# "MetafileFormat" özelliğini "HtmlMetafileFormat.Svg" olarak ayarlayarak bir SVG nesnesi olarak korumak.
# "MetafileFormat" özelliğini "HtmlMetafileFormat.EmfOrWmf" olarak ayarlayarak bir metafile'a dönüştürmek.
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

