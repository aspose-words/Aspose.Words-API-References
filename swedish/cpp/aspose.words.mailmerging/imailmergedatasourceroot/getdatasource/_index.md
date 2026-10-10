---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource metod"
linktitle: "GetDataSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource metod. Aspose.Words mailmerge‑motor anropar denna metod när den stöter på början av ett top‑nivå mailmerge‑område i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Den Aspose.Words‑motor för kopplad sammanslagning anropar den här metoden när den stöter på början av ett top‑nivå sammanslagningsområde.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableName | System::String | Namnet på mail‑sammanfogningsregionen enligt angivet i mall‑dokumentet. Skiftlägesokänslig. |

### ReturnValue

Ett datakällobjekt som ger åtkomst till data‑poster i den angivna tabellen.
## Anmärkningar


När Aspose.Words mailmerge‑motorerna fyller ett dokument med data och stöter på MERGEFIELD TableStart:TableName, anropar de [GetDataSource()](./) på detta objekt. Din implementation måste returnera ett nytt datakällobjekt. Aspose.Words kommer att använda den returnerade datakällan för att fylla mailmerge‑området.

Om en datakälla (tabell) med det angivna namnet inte finns, bör din implementation returnera **null**.

## Se även

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
