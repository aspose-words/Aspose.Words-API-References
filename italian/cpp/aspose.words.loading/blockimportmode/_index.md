---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::BlockImportMode enum. Specifica come le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Specifica come le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML.

```cpp
enum class BlockImportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) dei blocchi genitore vengono uniti e memorizzati negli elementi figlio (ad esempio paragrafi o tabelle). |
| Preserve | 1 | [Properties](../../aspose.words.properties/) dei blocchi genitore vengono importati in una struttura logica speciale e sono memorizzati separatamente dai nodi del documento. |


## Esempi



Mostra come le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Imposta la nuova modalità di importazione degli elementi a livello di blocco HTML.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
