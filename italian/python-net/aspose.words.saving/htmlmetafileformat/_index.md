---
title: HtmlMetafileFormat enumeration
linktitle: HtmlMetafileFormat enumeration
articleTitle: HtmlMetafileFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlMetafileFormat enumeration. Indicates the format in which metafiles are saved to HTML documents."
type: docs
weight: 260
url: /it/python-net/aspose.words.saving/htmlmetafileformat/
---

## HtmlMetafileFormat enumeration

Indicates the format in which metafiles are saved to HTML documents.


### Members

| Name | Description |
| --- | --- |
| PNG | Metafiles are rendered to raster PNG images. |
| SVG | Metafiles are converted to vector SVG images. |
| EMF_OR_WMF | Metafiles are saved as is, without conversion. |

### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```python
html = "<html>\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\n                    </svg>\n                </html>"
# Usa 'ConvertSvgToEmf' per ripristinare il comportamento legacy
# dove tutte le immagini SVG caricate da un documento HTML venivano convertite in EMF.
# Ora le immagini SVG sono caricate senza conversione
# se la versione di MS Word specificata nelle opzioni di caricamento supporta nativamente le immagini SVG.
load_options = aw.loading.HtmlLoadOptions()
load_options.convert_svg_to_emf = True
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=load_options)
# Questo documento contiene un elemento <svg> sotto forma di testo.
# Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
# per determinare come l'operazione di salvataggio gestisce questo oggetto.
# Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.Png" per convertirlo in un'immagine PNG.
# Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.Svg" per conservarlo come oggetto SVG.
# Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.EmfOrWmf" per convertirlo in un metafile.
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

* module [aspose.words.saving](../)

