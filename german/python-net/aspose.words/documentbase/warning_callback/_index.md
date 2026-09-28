---
title: DocumentBase.warning_callback property
linktitle: warning_callback property
articleTitle: warning_callback property
second_title: Aspose.Words for Python
description: "DocumentBase.warning_callback property. Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss."
type: docs
weight: 100
url: /de/python-net/aspose.words/documentbase/warning_callback/
---

## DocumentBase.warning_callback property

Called during various document processing procedures when an issue is detected that might result
in data or formatting fidelity loss.


```python
@property
def warning_callback(self) -> aspose.words.IWarningCallback:
    ...

@warning_callback.setter
def warning_callback(self, value: aspose.words.IWarningCallback):
    ...

```

### Remarks

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as
early as possible to avoid the warnings loss. E.g. such properties as [Document.page_count](../../document/page_count/)
actually build the document layout which is used later for rendering, and the layout warnings may be lost if
warning callback is specified just for the rendering calls later.



### Examples

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
callback = self.FontSubstitutionWarningCollector()
doc.warning_callback = callback
# Speichern Sie die aktuelle Sammlung von Schriftquellen, die die Standardschriftquelle für jedes Dokument sein wird
# für die wir keine andere Schriftquelle angeben.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Zu Testzwecken setzen wir Aspose.Words so, dass es nur in einem Ordner nach Schriften sucht, der nicht existiert.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# Beim Rendern des Dokuments gibt es keinen Ort, an dem die Schriftart "Times New Roman" gefunden werden kann.
# Dies führt zu einer Schriftart‑Ersetzungswarnung, die unser Callback erkennt.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Öffnen Sie ein Dokument, das Text enthält, der mit einer Schrift formatiert ist, die in keiner unserer Schriftquellen existiert.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Weisen Sie einen Rückruf zu, um Warnungen zur Schrift­substitution zu behandeln.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Legen Sie einen Standard‑Schriftartnamen fest und aktivieren Sie die Schrift­substitution.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Ursprüngliche Schriftmetriken sollten nach der Schrift­substitution verwendet werden.
doc.layout_options.keep_original_font_metrics = True
# Wir erhalten eine Schrift­substitutionswarnung, wenn wir ein Dokument mit einer fehlenden Schrift speichern.
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings (FontSubstitutionWarningCollector).

```python
class FontSubstitutionWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
            self.font_substitution_warnings.warning(info)
```

### See Also

* module [aspose.words](../../)
* class [DocumentBase](../)

