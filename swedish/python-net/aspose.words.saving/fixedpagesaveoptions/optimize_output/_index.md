---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /sv/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(file_name=MY_DIR + 'Unoptimized document.docx')
# Skapa ett "XpsSaveOptions"-objekt för att skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .XPS.
save_options = aw.saving.XpsSaveOptions()
# Ställ in egenskapen "OptimizeOutput" till "true" för att vidta åtgärder såsom att ta bort nästlade eller tomma dukar
# och sammanfoga intilliggande körningar med identisk formatering för att optimera utdata-dokumentets innehåll.
# Detta kan påverka dokumentets utseende.
# Ställ in egenskapen "OptimizeOutput" till "false" för att spara dokumentet normalt.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

