---
title: "Enum Aspose::Words::HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::HtmlInsertOptions enum. Specifica le opzioni per il metodo InsertHtml() in C++."
type: docs
weight: 92000
url: /it/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Specifica le opzioni per il metodo [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Utilizza le opzioni predefinite durante l'inserimento di HTML. |
| UseBuilderFormatting | 1 | Utilizza la formattazione di carattere e paragrafo specificata in [DocumentBuilder](../documentbuilder/) come formattazione di base per il testo inserito da HTML. |
| RemoveLastEmptyParagraph | 2 | Rimuove il paragrafo vuoto che viene normalmente inserito dopo l'HTML che termina con un elemento di livello blocco. |
| PreserveBlocks | 4 | Preserva le proprietà degli elementi di livello blocco. |


## Esempi



Mostra come consentire una migliore conservazione dei bordi e dei margini visualizzati.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Imposta la nuova modalità di importazione degli elementi a livello di blocco HTML.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
