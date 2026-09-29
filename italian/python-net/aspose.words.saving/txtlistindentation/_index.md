---
title: TxtListIndentation class
linktitle: TxtListIndentation class
articleTitle: TxtListIndentation class
second_title: Aspose.Words for Python
description: "aspose.words.saving.TxtListIndentation class. Specifies how list levels are indented when document is exporting to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT) format"
type: docs
weight: 880
url: /it/python-net/aspose.words.saving/txtlistindentation/
---

## TxtListIndentation class

Specifies how list levels are indented when document is exporting to [SaveFormat.TEXT](../../aspose.words/saveformat/#TEXT) format.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/python-net/save-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [TxtListIndentation()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [character](./character/) | Gets or sets which character to use for indenting list levels. The default value is '\\0', that means there is no indentation. |
| [count](./count/) | Gets or sets how many [TxtListIndentation.character](./character/) to use as indentation per one list level. The default value is 0, that means no indentation. |

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un elenco con tre livelli di rientro.
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui salviamo il documento in testo semplice.
txt_save_options = aw.saving.TxtSaveOptions()
# Imposta la proprietà "Character" per assegnare un carattere da utilizzare
# per il riempimento che simula il rientro dell'elenco in testo semplice.
txt_save_options.list_indentation.character = ' '
# Imposta la proprietà "Count" per specificare il numero di volte
# per inserire il carattere di riempimento per ogni livello di rientro dell'elenco.
txt_save_options.list_indentation.count = 3
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt')
new_line = system_helper.environment.Environment.new_line()
self.assertEqual(f'1. Item 1{new_line}' + f'   a. Item 2{new_line}' + f'      i. Item 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../)

