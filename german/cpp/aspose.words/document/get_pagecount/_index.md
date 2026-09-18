---
title: "Aspose::Words::Document::get_PageCount-Methode"
linktitle: "get_PageCount"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_PageCount-Methode. Gibt die Anzahl der Seiten im Dokument zurück, wie sie durch die zuletzt durchgeführte Seitenlayout‑Operation in C++ berechnet wurde."
type: docs
weight: 43000
url: /de/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


Liest die Anzahl der Seiten im Dokument, wie sie durch die zuletzt durchgeführte Seitenlayout-Operation berechnet wurde.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## Beispiele



Zeigt, wie man die Anzahl der Seiten im Dokument zählt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// Überprüfen Sie die erwartete Seitenzahl des Dokuments.
ASSERT_EQ(3, doc->get_PageCount());

// Das Abrufen der PageCount‑Eigenschaft löste das Seitenlayout des Dokuments aus, um den Wert zu berechnen.
// Dieser Vorgang muss beim Rendern des Dokuments in ein festes Seiten‑Speicherformat nicht erneut durchgeführt werden,
// wie .pdf. So können Sie etwas Zeit sparen, insbesondere bei komplexeren Dokumenten.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
