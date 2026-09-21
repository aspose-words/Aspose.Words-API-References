---
title: "Aspose::Words::Layout namnrymd"
linktitle: "Aspose::Words::Layout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout namnrymd. Namnrymden **Aspose.Words.Layout** tillhandahåller klasser som möjliggör åtkomst till information såsom på vilken sida och var på en sida specifika dokumentelement är placerade när dokumentet formateras till sidor i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.layout/
---

Namnområdet **Aspose.Words.Layout** tillhandahåller klasser som möjliggör åtkomst till information såsom på vilken sida och var på en sida specifika dokumentelement är placerade när dokumentet formateras till sidor.

## Klasser

| Klass | Beskrivning |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Denna klass möjliggör beräkning av sidnummer för dokumentnoder. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | Enumererar sidlayout‑entiteter i ett dokument. Du kan använda denna klass för att gå igenom sidlayoutmodellen. Tillgängliga egenskaper är typ, geometri, text och sidindex där entiteten renderas, samt den övergripande strukturen och relationerna. Använd en kombination av [GetEntity()](../) och [Current](./layoutenumerator/get_current/) för att gå till den entitet som motsvarar en dokumentnod. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | Innehåller de alternativ som möjliggör styrning av dokumentlayoutprocessen. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Ett argument som skickas till [Notify()](./ipagelayoutcallback/notify/) För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | Tillåter att kontrollera hur dokumentrevisioner hanteras under layoutprocessen. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## Gränssnitt

| Gränssnitt | Beskrivning |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implementera detta gränssnitt om du vill ha din egen anpassade metod som anropas under byggandet och renderingen av sidlayoutmodellen. |
## Enums

| Enum | Beskrivning |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Anger renderingsläget för dokumentkommentarer. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Representerar olika beteenden när sidnummer beräknas i ett kontinuerligt avsnitt som startar om sidnumreringen. |
| [LayoutEntityType](./layoutentitytype/) | Typer av layout‑entiteter. |
| [PageLayoutEvent](./pagelayoutevent/) | En kod för händelse som utlöses under byggandet och renderingen av sidlayoutmodellen. Sidlayoutmodellen byggs i två steg. Först, "conversion step", vilket är när sidlayouten hämtar dokumentinnehåll och skapar ett objekt‑graf. Andra, "reflow step", vilket är när strukturer delas, slås ihop och ordnas i sidor. Beroende på vilken operation som utlöste byggandet kan sidlayoutmodellen eventuellt renderas vidare till fast sidformat eller inte. Till exempel kräver beräkning av antalet sidor i dokumentet eller uppdatering av fält ingen rendering, medan export till Pdf gör det. |
| [RevisionColor](./revisioncolor/) | Tillåter att ange färg för dokumentrevisioner. |
| [RevisionTextEffect](./revisiontexteffect/) | Tillåter att ange dekorationseffekt för revisioner av dokumenttext. |
| [ShowInBalloons](./showinballoons/) | Anger vilka revisioner som renderas i ballonger. |
