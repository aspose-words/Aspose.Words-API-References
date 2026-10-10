---
title: HtmlLoadOptions.convert_svg_to_emf property
linktitle: convert_svg_to_emf property
articleTitle: convert_svg_to_emf property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.convert_svg_to_emf property. Gets or sets a value indicating whether to convert loaded SVG images to the EMF format"
type: docs
weight: 30
url: /es/python-net/aspose.words.loading/htmlloadoptions/convert_svg_to_emf/
---

## HtmlLoadOptions.convert_svg_to_emf property

Gets or sets a value indicating whether to convert loaded SVG images to the EMF format.
Default value is ``False`` and, if possible, loaded SVG images are stored as is without conversion.



```python
@property
def convert_svg_to_emf(self) -> bool:
    ...

@convert_svg_to_emf.setter
def convert_svg_to_emf(self, value: bool):
    ...

```

### Remarks

Newer versions of MS Word support SVG images natively. If the MS Word version specified in load options supports
SVG, Aspose.Words will store SVG images as is without conversion. If SVG is not supported, loaded SVG images will be
converted to the EMF format.

If, however, this option is set to ``True``, Aspose.Words will convert loaded SVG images to EMF even if SVG
images are supported by the specified version of MS Word.





### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```python
html = "<html>\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\n                    </svg>\n                </html>"
# Utilice 'ConvertSvgToEmf' para revertir el comportamiento heredado
# donde todas las imágenes SVG cargadas desde un documento HTML se convertían a EMF.
# Ahora las imágenes SVG se cargan sin conversión
# si la versión de MS Word especificada en las opciones de carga admite imágenes SVG de forma nativa.
load_options = aw.loading.HtmlLoadOptions()
load_options.convert_svg_to_emf = True
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=load_options)
# Este documento contiene un elemento <svg> en forma de texto.
# Al guardar el documento en HTML, podemos pasar un objeto SaveOptions
# para determinar cómo maneja la operación de guardado este objeto.
# Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.Png" para convertirlo en una imagen PNG.
# Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.Svg" lo preserva como un objeto SVG.
# Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.EmfOrWmf" para convertirlo en un metarchivo.
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

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

