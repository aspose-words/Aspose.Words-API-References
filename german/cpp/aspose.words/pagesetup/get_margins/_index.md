---
title: "Aspose::Words::PageSetup::get_Margins Methode"
linktitle: "get_Margins"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_Margins Methode. Gibt voreingestellte Ränder der Seite zurück oder legt sie fest in C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


Gibt voreingestellte [Ränder](../../margins/) der Seite zurück oder legt sie fest.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


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

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
