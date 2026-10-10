---
title: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource metod"
linktitle: "GetChildDataSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource metod. Aspose.Words‑motor för mail‑sammanfogning anropar denna metod när den stöter på början av en inbäddad mail‑sammanfogningsregion i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Aspose.Words‑motor för kopplad utskrift anropar den här metoden när den stöter på början av ett nästlat kopplat utskriftsområde.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableName | System::String | Namnet på mail‑sammanfogningsregionen enligt angivet i mall‑dokumentet. Skiftlägesokänslig. |

### ReturnValue

Ett datakällobjekt som ger åtkomst till data‑poster i den angivna tabellen.
## Anmärkningar


När Aspose.Words‑motorerna för mail‑sammanfogning fyller en mail‑sammanfogningsregion med data och stöter på början av en inbäddad mail‑sammanfogningsregion i formen MERGEFIELD TableStart:TableName, anropar den [GetChildDataSource()](./) på det aktuella datakällobjektet. Din implementation måste returnera ett nytt datakällobjekt som ger åtkomst till underposterna för den aktuella föräldraposten. Aspose.Words kommer att använda den returnerade datakällan för att fylla den inbäddade mail‑sammanfogningsregionen.

Nedan följer reglerna som implementeringen av [GetChildDataSource()](./) måste följa.

Om tabellen som representeras av detta datakällobjekt har en relaterad under‑ (detalj‑)tabell med det angivna namnet, måste din implementation returnera ett nytt [IMailMergeDataSource](../)‑objekt som ger åtkomst till underposterna för den aktuella posten. Ett exempel på detta är relationen Orders / OrderDetails. Låt oss anta att det aktuella [IMailMergeDataSource](../)‑objektet representerar Orders‑tabellen och att det har en aktuell orderpost. Därefter stöter Aspose.Words på \"MERGEFIELD TableStart:OrderDetails\" i dokumentet och anropar [GetChildDataSource()](./). Du måste skapa och returnera ett [IMailMergeDataSource](../)‑objekt som gör det möjligt för Aspose.Words att komma åt OrderDetails‑posten för den aktuella ordern.

Om detta datakällobjekt inte har en relation till tabellen med det angivna namnet, måste du returnera ett [IMailMergeDataSource](../)‑objekt som ger åtkomst till alla poster i den angivna tabellen.

Om en tabell med det angivna namnet inte finns, bör din implementation returnera **null**.

## Se även

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
