---
title: LoadOptions.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "LoadOptions.font_settings property. Allows to specify document font settings."
type: docs
weight: 60
url: /it/python-net/aspose.words.loading/loadoptions/font_settings/
---

## LoadOptions.font_settings property

Allows to specify document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words
may resolve the fonts to perform font fallback.

If set to ``None``, default static font settings [FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how to designate font substitutes during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.font_settings = aw.fonts.FontSettings()
# Imposta una regola di sostituzione dei caratteri per un oggetto LoadOptions.
# Se il documento che stiamo caricando utilizza un carattere che non possediamo,
# questa regola sostituirà il carattere non disponibile con uno che esiste.
# In questo caso, tutte le occorrenze di "MissingFont" verranno convertite in "Comic Sans MS".
substitution_rule = load_options.font_settings.substitution_settings.table_substitution
substitution_rule.add_substitutes('MissingFont', ['Comic Sans MS'])
doc = aw.Document(file_name=MY_DIR + 'Missing font.html', load_options=load_options)
# A questo punto tale testo sarà ancora in "MissingFont".
# La sostituzione dei caratteri avverrà quando renderizziamo il documento.
self.assertEqual('MissingFont', doc.first_section.body.first_paragraph.runs[0].font.name)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.ResolveFontsBeforeLoadingDocument.pdf')
```

Shows how to apply font substitution settings while loading a document.

```python
# Crea un oggetto FontSettings che sostituirà il carattere "Times New Roman"
# con il carattere "Arvo" dalla nostra cartella "MyFonts".
font_settings = aw.fonts.FontSettings()
font_settings.set_fonts_folder(FONTS_DIR, False)
font_settings.substitution_settings.table_substitution.add_substitutes('Times New Roman', ['Arvo'])
# Imposta quell'oggetto FontSettings come proprietà di un nuovo oggetto LoadOptions.
load_options = aw.loading.LoadOptions()
load_options.font_settings = font_settings
# Carica il documento, quindi renderizzalo come PDF con la sostituzione dei caratteri.
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'LoadOptions.FontSettings.pdf')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

