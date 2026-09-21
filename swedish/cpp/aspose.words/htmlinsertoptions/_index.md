---
title: "Aspose::Words::HtmlInsertOptions enum"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::HtmlInsertOptions enum. Anger alternativ för metoden InsertHtml() i C++."
type: docs
weight: 92000
url: /sv/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Anger alternativ för metoden [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Använd standardalternativen när du infogar HTML. |
| UseBuilderFormatting | 1 | Använd teckensnitt- och styckeformatering som anges i [DocumentBuilder](../documentbuilder/) som grundformatering för text som infogas från HTML. |
| RemoveLastEmptyParagraph | 2 | Ta bort det tomma stycket som normalt infogas efter HTML som avslutas med ett blocknivåelement. |
| PreserveBlocks | 4 | Bevara egenskaper för blocknivåelement. |


## Exempel



Visar hur man bättre bevarar kanter och marginaler som syns.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Ställ in det nya läget för import av HTML‑blocknivåelement.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
