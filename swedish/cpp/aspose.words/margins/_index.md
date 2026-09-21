---
title: "Aspose::Words::Margins enum"
linktitle: "Marginaler"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Margins enum. Anger förinställda marginaler i C++."
type: docs
weight: 99000
url: /sv/cpp/aspose.words/margins/
---
## Margins enum


Anger förinställda marginaler.

```cpp
enum class Margins
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | 0 | Normala marginaler. |
| Smal | 1 | Smala marginaler. |
| Måttlig | 2 | Måttliga marginaler. |
| Bred | 3 | Breda marginaler. |
| Speglad | 4 | Speglade marginaler. |
| Anpassad | 5 | Anpassade marginaler. |


## Exempel



Visar när man ska beräkna om sidlayouten för dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Att spara ett dokument till PDF, till en bild eller skriva ut för första gången kommer automatiskt
// cacha layouten för dokumentet inom dess sidor.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// I den nuvarande versionen av Aspose.Words återuppbyggs inte dokumentet automatiskt när det ändras
// den cachade sidlayouten. Om vi vill att den cachade layouten
// ska hållas uppdaterad, måste vi uppdatera den manuellt.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
