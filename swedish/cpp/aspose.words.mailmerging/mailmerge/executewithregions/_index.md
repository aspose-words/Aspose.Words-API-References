---
title: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions metod"
linktitle: "ExecuteWithRegions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions metod. Utför en kopplad utskrift från en anpassad datakälla med kopplade utskriftsregioner i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Utför en koppling från en anpassad datakälla med kopplingsregioner.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Ett objekt som implementerar det anpassade gränssnittet för sammanslagningsdatakälla. |
## Anmärkningar


Använd den här metoden för att fylla kopplade utskriftsfält i dokumentet med värden från någon anpassad datakälla, såsom en XML‑fil eller samlingar av affärsobjekt. Du måste skriva din egen klass som implementerar gränssnittet [IMailMergeDataSource](../../imailmergedatasource/).

Du kan använda den här metoden endast när [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) är **false**, det vill säga när du inte behöver stöd för språk som skrivs från höger till vänster (såsom arabiska eller hebreiska).

## Se även

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Utför en koppling från en anpassad datakälla med kopplingsregioner.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Ett objekt som implementerar det anpassade gränssnittet för rot av mail merge‑datakälla. |
## Anmärkningar


Använd den här metoden för att fylla kopplade utskriftsfält i dokumentet med värden från någon anpassad datakälla, såsom en XML‑fil eller samlingar av affärsobjekt. Du måste skriva dina egna klasser som implementerar gränssnitten [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) och [IMailMergeDataSource](../../imailmergedatasource/).

Du kan använda den här metoden endast när [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) är **false**, det vill säga när du inte behöver stöd för språk som skrivs från höger till vänster (såsom arabiska eller hebreiska).

## Se även

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
