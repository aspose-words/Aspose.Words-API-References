---
title: "Aspose::Words::HtmlInsertOptions enum"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::HtmlInsertOptions enum. Gibt Optionen für die Methode InsertHtml() in C++ an."
type: docs
weight: 92000
url: /de/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Gibt Optionen für die Methode [InsertHtml()](../) an.

```cpp
enum class HtmlInsertOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Verwenden Sie die Standardoptionen beim Einfügen von HTML. |
| UseBuilderFormatting | 1 | Verwenden Sie die in [DocumentBuilder](../documentbuilder/) angegebene Schrift- und Absatzformatierung als Basisformatierung für aus HTML eingefügten Text. |
| RemoveLastEmptyParagraph | 2 | Entfernt den leeren Absatz, der normalerweise nach HTML eingefügt wird, das mit einem Block-Element endet. |
| PreserveBlocks | 4 | Erhält die Eigenschaften von Block-Elementen. |


## Beispiele



Zeigt, wie man eine bessere Erhaltung von Rahmen und Rändern ermöglicht.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Setzt den neuen Modus für den Import von HTML-Blockelementen.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
