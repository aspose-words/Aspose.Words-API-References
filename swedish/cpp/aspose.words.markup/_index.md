---
title: "Aspose::Words::Markup namnrymd."
linktitle: "Aspose::Words::Markup"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup namnrymd. Aspose.Words.Markup‑namnrymden innehåller klasser som representerar kunddefinierad semantik i ett dokument: smarta taggar, anpassad XML och strukturerade dokumenttaggar (innehållskontroller) i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.markup/
---

Namnområdet **Aspose.Words.Markup** innehåller klasser som representerar kunddefinierad semantik i ett dokument: smarta taggar, anpassad XML och strukturerade dokumenttaggar (innehållskontroller).

## Klasser

| Klass | Beskrivning |
| --- | --- |
| [CustomPart](./custompart/) | Representerar en anpassad (godtycklig innehålls)del som inte definieras av ISO/IEC 29500-standarden. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomPartCollection](./custompartcollection/) | Representerar en samling av [CustomPart](./custompart/)-objekt. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPart](./customxmlpart/) | Representerar en anpassad XML‑datalagringsdel (anpassad XML‑data inom ett paket). För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Representerar en samling av anpassade XML‑delar. Objektet är [CustomXmlPart](./customxmlpart/)-objekt. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlProperty](./customxmlproperty/) | Representerar ett enda anpassat XML-attribut eller en smart tag‑egenskap. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Representerar en samling av anpassade XML-attribut eller smart tag‑egenskaper. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | En samling strängar som representerar XML‑scheman som är associerade med en anpassad XML‑del. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItem](./sdtlistitem/) | Detta element specificerar ett enda listobjekt inom en föräldra-[ComboBox](./sdttype/) eller [DropDownList](./sdttype/) strukturerad dokumenttagg. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItemCollection](./sdtlistitemcollection/) | Tillhandahåller åtkomst till [SdtListItem](./sdtlistitem/)‑element i en strukturerad dokumenttagg. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SmartTag](./smarttag/) | Detta element specificerar förekomsten av en smart tag runt en eller flera inline‑strukturer (körningar, bilder, fält, osv.) inom ett stycke. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTag](./structureddocumenttag/) | Representerar en strukturerad dokumenttagg (SDT eller innehållskontroll) i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | En samling av [IStructuredDocumentTag](./istructureddocumenttag/)‑instanser som representerar de strukturerade dokumenttaggarna i det angivna intervallet. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Representerar ett slut på en **ranged** strukturerad dokumenttagg som accepterar innehåll med flera sektioner. Se även noden [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Representerar starten på en **ranged** strukturerad dokumenttagg som accepterar innehåll med flera sektioner. Se även [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/). För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [XmlMapping](./xmlmapping/) | Specificerar den information som används för att etablera en mappning mellan den överordnade strukturerade dokumenttaggen och ett XML‑element som lagras i en anpassad XML‑datadel i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
## Gränssnitt

| Gränssnitt | Beskrivning |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Gränssnitt för att definiera gemensam data för [StructuredDocumentTag](./structureddocumenttag/) och [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). |
## Enums

| Enum | Beskrivning |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Anger nivån i dokumentträdet där en viss [StructuredDocumentTag](./structureddocumenttag/) kan förekomma. |
| [SdtAppearance](./sdtappearance/) | Anger utseendet på en strukturerad dokumenttagg. |
| [SdtCalendarType](./sdtcalendartype/) | Anger de möjliga kalendertyperna som kan användas för att specificera [CalendarType](./structureddocumenttag/get_calendartype/) i ett Office Open XML-dokument. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Anger hur datumet för en datum‑SDT lagras/hämtas när SDT:n är bunden till en XML‑nod i dokumentets datalager. |
| [SdtType](./sdttype/) | Anger typen av en strukturerad dokumenttagg (SDT)-nod. |
