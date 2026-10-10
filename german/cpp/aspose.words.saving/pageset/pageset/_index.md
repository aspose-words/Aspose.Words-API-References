---
title: "Aspose::Words::Saving::PageSet::PageSet-Konstruktor"
linktitle: "PageSet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageSet::PageSet-Konstruktor. Erstellt ein Seitenset basierend auf genauen Seitenindizes in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/pageset/pageset/
---
## PageSet::PageSet(const System::ArrayPtr\<int32_t\>\&) constructor


Erstellt ein Seitenset basierend auf genauen Seitenindizes.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<int32_t> &pages)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Seiten | const System::ArrayPtr\<int32_t\>\& | Nullbasierte Indizes der Seiten. |

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

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) constructor


Erstellt ein Seitenset basierend auf Bereichen.

```cpp
Aspose::Words::Saving::PageSet::PageSet(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Saving::PageRange>> &ranges)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bereiche | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\& | Array von Seitenbereichen. |

## Beispiele



Zeigt, wie Seiten basierend auf genauen PageRanges extrahiert werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## Siehe auch

* Class [PageRange](../../pagerange/)
* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PageSet::PageSet(int32_t) constructor


Erstellt ein einseitiges Set basierend auf einem genauen Seitenindex.

```cpp
Aspose::Words::Saving::PageSet::PageSet(int32_t page)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Seite | int32_t | Nullbasierter Index der Seite. |

## Beispiele



Zeigt, wie man eine Seite eines Dokuments in ein JPEG‑Bild rendert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Erstellen Sie ein "ImageSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
// um die Art und Weise zu ändern, wie diese Methode das Dokument in ein Bild rendert.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Setzen Sie "PageSet" auf "1", um die zweite Seite auszuwählen über
// den nullbasierten Index, um mit dem Rendern des Dokuments zu beginnen.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Wenn wir das Dokument im JPEG‑Format speichern, rendert Aspose.Words nur eine Seite.
// Dieses Bild enthält eine Seite, beginnend mit Seite zwei,
// die lediglich die zweite Seite des Originaldokuments ist.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## Siehe auch

* Class [PageSet](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
