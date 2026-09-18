---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet Methode"
linktitle: "get_PageSet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet Methode. Gibt die zu rendernden Seiten zurück oder legt sie fest. Standard ist, dass alle Seiten im Dokument in C++ verwendet werden."
type: docs
weight: 9000
url: /de/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Ruft die zu rendernden Seiten ab oder legt sie fest. Standard ist, dass alle Seiten im Dokument gerendert werden.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Beispiele



Zeigt, wie man Seiten basierend auf genauen Seitenindizes extrahiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie dem Dokument fünf Seiten hinzu.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Erstellen Sie ein \"XpsSaveOptions\"-Objekt, das wir an die \"Save\"-Methode des Dokuments übergeben können.
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Verwenden Sie die \"PageSet\"-Eigenschaft, um eine Menge der Seiten des Dokuments auszuwählen, die in die Ausgabedatei XPS gespeichert werden sollen.
// In diesem Fall wählen wir über einen nullbasierten Index nur drei Seiten aus: Seite 1, Seite 2 und Seite 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Siehe auch

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
