---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize‑metoden"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize‑metoden. Anger om bilder skalas av Aspose.Words till den omgivande formens storlek vid export till HTML, MHTML eller EPUB. Standardvärdet är true i C++."
type: docs
weight: 46000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Anger om bilder skalas av Aspose.Words till den omgivande formens storlek vid export till HTML, MHTML eller EPUB. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Anmärkningar


En bild i ett Microsoft Word‑dokument är en form. Formen har en storlek och bilden har sin egen storlek. Storlekarna är inte direkt länkade. Till exempel kan bilden vara 1024 × 786 pixlar, men formen som visar bilden kan vara 400 × 300 punkter.

För att visa en bild i webbläsaren måste den skalas till formens storlek. Egenskapen [ScaleImageToShapeSize](./) styr var bildskalningen sker: i Aspose.Words under export till HTML eller i webbläsaren när dokumentet visas.

När [ScaleImageToShapeSize](./) är **true** skalas bilden av [Aspose.Words](../../../aspose.words/) med högkvalitativ skalning under export till HTML. När [ScaleImageToShapeSize](./) är **false** exporteras bilden med sin ursprungliga storlek och webbläsaren måste skala den.

Generellt utför webbläsare snabb och lågkvalitativ skalning. Som ett resultat får du normalt bättre visningskvalitet i webbläsaren och mindre filstorlek när [ScaleImageToShapeSize](./) är **true**, men bättre utskriftskvalitet och snabbare konvertering när [ScaleImageToShapeSize](./) är **false**.

Förutom former som innehåller enskilda rasterbilder påverkar detta alternativ även gruppformer som består av rasterbilder. Om [ScaleImageToShapeSize](./) är **false** och en gruppform innehåller rasterbilder vars inneboende upplösning är högre än värdet som anges i [ImageResolution](../get_imageresolution/), kommer Aspose.Words att öka renderingsupplösningen för den gruppen. Detta gör det möjligt att bättre bevara kvaliteten på grupperade högupplösta bilder när de sparas till HTML.

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
