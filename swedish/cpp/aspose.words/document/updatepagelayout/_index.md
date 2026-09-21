---
title: "Aspose::Words::Document::UpdatePageLayout metod"
linktitle: "UpdatePageLayout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::UpdatePageLayout metod. Återuppbygger sidlayouten för dokumentet i C++."
type: docs
weight: 98000
url: /sv/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


Bygger om sidlayouten för dokumentet.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## Anmärkningar


Denna metod formaterar ett dokument till sidor och uppdaterar sidnummerrelaterade fält i dokumentet såsom PAGE, PAGES, PAGEREF och REF. Den aktuella sidlayoutinformationen krävs för en korrekt rendering av dokumentet till fastsidiga format.

Denna metod anropas automatiskt när du först konverterar ett dokument till PDF, XPS, bild eller skriver ut det. Men om du ändrar dokumentet efter rendering och sedan försöker rendera det igen – Aspose.Words uppdaterar inte sidlayouten automatiskt. I så fall bör du anropa [UpdatePageLayout](./) innan du renderar igen.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
