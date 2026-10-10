---
title: "Aspose::Words::Document::ExtractPages Methode"
linktitle: "ExtractPages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::ExtractPages Methode. Gibt das Document-Objekt zurück, das den angegebenen Seitenbereich in C++ darstellt."
type: docs
weight: 12000
url: /de/cpp/aspose.words/document/extractpages/
---
## Document::ExtractPages(int32_t, int32_t) method


Gibt das [Document](../) Objekt zurück, das den angegebenen Seitenbereich darstellt.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| count | int32_t | Anzahl der zu extrahierenden Seiten. |

## Beispiele



Zeigt, wie man einen angegebenen Seitenbereich aus dem Dokument erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Layout entities.docx");

doc = doc->ExtractPages(0, 2);

doc->Save(get_ArtifactsDir() + u"Document.ExtractPages.docx");
```


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

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::ExtractPages(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) method


Gibt das [Document](../) Objekt zurück, das den angegebenen Seitenbereich und die angegebenen Extraktionsoptionen darstellt.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::ExtractPages(int32_t index, int32_t count, const System::SharedPtr<Aspose::Words::PageExtractOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| count | int32_t | Anzahl der zu extrahierenden Seiten. |
| options | const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\& | Stellt Optionen zur Verwaltung des Seitenextraktionsvorgangs bereit. |

## Siehe auch

* Class [Document](../)
* Class [PageExtractOptions](../../pageextractoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
