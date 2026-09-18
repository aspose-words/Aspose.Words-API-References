---
title: "Aspose::Words::Document::UpdatePageLayout Methode"
linktitle: "UpdatePageLayout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::UpdatePageLayout Methode. Baut das Seitenlayout des Dokuments in C++ neu auf."
type: docs
weight: 98000
url: /de/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Erstellt das Seitenlayout des Dokuments neu.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Hinweise


Diese Methode formatiert ein Dokument in Seiten und aktualisiert die seitenzahlbezogenen Felder im Dokument wie PAGE, PAGES, PAGEREF und REF. Die aktuelle Seitenlayout‑Information ist für eine korrekte Darstellung des Dokuments in fest‑Seiten‑Formaten erforderlich.

Diese Methode wird automatisch aufgerufen, wenn Sie ein Dokument erstmals in PDF, XPS, Bild konvertieren oder drucken. Wenn Sie das Dokument jedoch nach der Darstellung ändern und anschließend erneut rendern – Aspose.Words wird das Seitenlayout nicht automatisch aktualisieren. In diesem Fall sollten Sie vor dem erneuten Rendern [UpdatePageLayout](./) aufrufen.

## Beispiele



Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden muss.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Das Speichern eines Dokuments als PDF, als Bild oder das erstmalige Drucken wird automatisch
// Cache das Layout des Dokuments innerhalb seiner Seiten.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Das Dokument auf irgendeine Weise ändern.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// In der aktuellen Version von Aspose.Words wird das Dokument beim Ändern nicht automatisch neu aufgebaut
// das zwischengespeicherte Seitenlayout. Wenn wir möchten, dass das zwischengespeicherte Layout
// auf dem neuesten Stand bleibt, müssen wir es manuell aktualisieren.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
