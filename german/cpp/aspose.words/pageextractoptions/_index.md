---
title: "Aspose::Words::PageExtractOptions Klasse"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageExtractOptions Klasse. Ermöglicht das Festlegen von Optionen für das Extrahieren von Dokumentseiten in C++."
type: docs
weight: 45500
url: /de/cpp/aspose.words/pageextractoptions/
---
## PageExtractOptions class


Ermöglicht das Festlegen von Optionen für das Extrahieren von Dokumentseiten.

```cpp
class PageExtractOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/)() const | Gibt an, ob NUMPAGES‑Felder im resultierenden Dokument durch ihre tatsächlichen Werte ersetzt werden. Standardwert ist **true**. |
| [get_UpdatePageStartingNumber](./get_updatepagestartingnumber/)() const | Gibt an, ob die Startseitennummer im resultierenden Dokument aktualisiert werden soll. Standardwert ist **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageExtractOptions](./pageextractoptions/)() |  |
| [set_UnlinkPagesNumberFields](./set_unlinkpagesnumberfields/)(bool) | Setter für [Aspose::Words::PageExtractOptions::get_UnlinkPagesNumberFields](./get_unlinkpagesnumberfields/). |
| [set_UpdatePageStartingNumber](./set_updatepagestartingnumber/)(bool) | Setter für [Aspose::Words::PageExtractOptions::get_UpdatePageStartingNumber](./get_updatepagestartingnumber/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
