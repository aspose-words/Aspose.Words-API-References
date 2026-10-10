---
title: "Aspose::Words::Saving::PageSet Klasse"
linktitle: "PageSet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageSet Klasse. Beschreibt eine zufällige Menge von Seiten. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words.saving/pageset/
---
## PageSet class


Beschreibt eine zufällige Menge von Seiten. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| static [get_All](./get_all/)() | Liefert eine Menge mit allen Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| static [get_Even](./get_even/)() | Ermittelt ein Set mit allen geraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| static [get_Odd](./get_odd/)() | Ermittelt ein Set mit allen ungeraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Erstellt ein einseitiges Set basierend auf einem genauen Seitenindex. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Erstellt ein Seitenset basierend auf genauen Seitenindizes. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Erstellt ein Seitenset basierend auf Bereichen. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
