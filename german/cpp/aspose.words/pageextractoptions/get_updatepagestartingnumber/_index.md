---
title: "Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber Methode"
linktitle: "get_UpdatePageStartingNumber"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber Methode. Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. Der Standardwert ist true in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/pageextractoptions/get_updatepagestartingnumber/
---
## PageExtractOptions::get_UpdatePageStartingNumber method


Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. Standardwert ist **true**.

```cpp
bool Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber() const
```


## Beispiele



Zeigt, wie die anfängliche Seitennummerierung zurückgesetzt und das NUMPAGE‑Feld gespeichert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Page fields.docx");

// Standardverhalten:
// Die extrahierte Seitennummerierung ist dieselbe wie im Originaldokument, als hätten wir in MS Word „2 Seiten drucken“ ausgewählt.
// Die Startseite wird auf 2 gesetzt und das Feld, das die Anzahl der Seiten angibt, wird entfernt
// und durch einen konstanten Wert ersetzt, der der Seitenanzahl entspricht.
System::SharedPtr<Aspose::Words::Document> extractedDoc1 = doc->ExtractPages(1, 1);
extractedDoc1->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Default.docx");

// Geändertes Verhalten:
// Die extrahierte Seitennummerierung wird zurückgesetzt und eine neue beginnt,
// als hätten wir den Inhalt der zweiten Seite kopiert und in ein neues Dokument eingefügt.
// Die Startseite wird auf 1 gesetzt und das Feld, das die Anzahl der Seiten angibt, bleibt unverändert
// und zeigt die aktuelle Seitenanzahl an.
auto extractOptions = System::MakeObject<Aspose::Words::PageExtractOptions>();
extractOptions->set_UpdatePageStartingNumber(false);
extractOptions->set_UnlinkPagesNumberFields(false);
System::SharedPtr<Aspose::Words::Document> extractedDoc2 = doc->ExtractPages(1, 1, extractOptions);
extractedDoc2->Save(get_ArtifactsDir() + u"Document.ExtractPagesWithOptions.Options.docx");
```

## Siehe auch

* Class [PageExtractOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
