---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::PageLayoutEvent enum. En kod för händelse som utlöses under byggandet och renderingen av sidlayoutmodellen. Sidlayoutmodellen byggs i två steg. Först, \"konverteringssteget\", då sidlayouten hämtar dokumentinnehåll och skapar ett objektgraf. Andra, \"omflödessteget\", då strukturer delas, slås ihop och ordnas i sidor. Beroende på vilken operation som utlöste byggandet kan sidlayoutmodellen eventuellt renderas vidare till ett fast sidformat eller inte. Till exempel kräver beräkning av antalet sidor i dokumentet eller uppdatering av fält ingen rendering, medan export till PDF gör det i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


En kod för händelse som utlöses under byggandet och renderingen av sidlayoutmodellen. Sidlayoutmodellen byggs i två steg. Först, "conversion step", vilket är när sidlayouten hämtar dokumentinnehåll och skapar ett objekt‑graf. Andra, "reflow step", vilket är när strukturer delas, slås ihop och ordnas i sidor. Beroende på vilken operation som utlöste byggandet kan sidlayoutmodellen eventuellt renderas vidare till fast sidformat eller inte. Till exempel kräver beräkning av antalet sidor i dokumentet eller uppdatering av fält ingen rendering, medan export till Pdf gör det.

```cpp
enum class PageLayoutEvent
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Standardvärde. |
| WatchDog | 1 | Motsvarar en kontrollpunkt i koden som ofta besöks och som är lämplig för att avbryta processen. Medan du är inne i [Notify()](../ipagelayoutcallback/notify/) kasta ett anpassat undantag för att avbryta processen. Du kan kasta när du hanterar någon återuppringningshändelse för att avbryta processen. Observera att om processen avbryts förblir sidlayoutmodellen i ett odefinierat tillstånd. Om processen avbryts vid omflöde av en hel sida, bör det dock vara möjligt att använda layoutmodellen fram till slutet av den sidan. |
| BuildStarted | 2 | Byggandet av sidlayouten har startat. Utlöst en gång. Detta är den första händelsen som inträffar när [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) anropas. |
| BuildFinished | 3 | Byggandet av sidlayouten har slutförts. Utlöst en gång. Detta är den sista händelsen som inträffar när [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) anropas. |
| ConversionStarted | 4 | Konverteringen av dokumentmodellen till sidlayout har startat. Utlöst en gång. Detta sker när layoutmodellen börjar hämta dokumentinnehåll. |
| ConversionFinished | 5 | Konverteringen av dokumentmodellen till sidlayout har slutförts. Utlöst en gång. Detta sker när layoutmodellen slutar hämta dokumentinnehåll. |
| ReflowStarted | 6 | Omflödet av sidlayouten har startat. Utlöst en gång. Detta sker när layoutmodellen börjar omflöda dokumentinnehåll. |
| ReflowFinished | 7 | Omflödet av sidlayouten har slutförts. Utlöst en gång. Detta sker när layoutmodellen slutar omflöda dokumentinnehåll. |
| PartReflowStarted | 8 | Omflödet av sidan har startat. Observera att sidan kan omflödas flera gånger och att omflödet kan starta om innan det är färdigt. |
| PartReflowFinished | 9 | Omflödet av sidan har slutförts. Observera att sidan kan omflödas flera gånger och att omflödet kan starta om innan det är färdigt. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) av sidan har startat. Detta utlöses en gång per sida. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) av sidan har slutförts. Detta utlöses en gång per sida. |

## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
