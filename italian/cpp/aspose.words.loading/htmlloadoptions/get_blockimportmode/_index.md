---
title: "Metodo Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode"
linktitle: "get_BlockImportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode. Ottiene o imposta un valore che specifica come vengono importate le proprietà degli elementi di livello blocco. Il valore predefinito è Merge in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


Ottiene o imposta un valore che specifica come vengono importate le proprietà degli elementi di livello blocco. Il valore predefinito è [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


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

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
