---
title: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource-Methode"
linktitle: "GetChildDataSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource-Methode. Die Seriendruck‑Engine von Aspose.Words ruft diese Methode auf, wenn sie den Beginn einer verschachtelten Seriendruckregion in C++ erkennt."
type: docs
weight: 3000
url: /de/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Die Aspose.Words Seriendruck‑Engine ruft diese Methode auf, wenn sie auf den Beginn einer verschachtelten Seriendruckregion stößt.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | System::String | Der Name der Seriendruckregion, wie im Vorlagendokument angegeben. Case‑insensitive. |

### ReturnValue

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle bietet.
## Hinweise


Wenn die Seriendruck‑Engines von Aspose.Words eine Seriendruckregion mit Daten füllen und dabei den Beginn einer verschachtelten Seriendruckregion in der Form MERGEFIELD TableStart:TableName erkennen, rufen sie [GetChildDataSource()](./) auf dem aktuellen Datenquellenobjekt auf. Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben, das Zugriff auf die Kinddatensätze des aktuellen übergeordneten Datensatzes bietet. Aspose.Words verwendet die zurückgegebene Datenquelle, um die verschachtelte Seriendruckregion zu füllen.

Im Folgenden sind die Regeln aufgeführt, die die Implementierung von [GetChildDataSource()](./) befolgen muss.

Wenn die Tabelle, die durch dieses Datenquellenobjekt dargestellt wird, eine zugehörige untergeordnete (Detail‑)Tabelle mit dem angegebenen Namen hat, muss Ihre Implementierung ein neues [IMailMergeDataSource](../)-Objekt zurückgeben, das Zugriff auf die Kinddatensätze des aktuellen Datensatzes bietet. Ein Beispiel dafür ist die Beziehung Orders / OrderDetails. Nehmen wir an, das aktuelle [IMailMergeDataSource](../)-Objekt stellt die Tabelle Orders dar und hat einen aktuellen Auftragsdatensatz. Anschließend stößt Aspose.Words im Dokument auf "MERGEFIELD TableStart:OrderDetails" und ruft [GetChildDataSource()](./) auf. Sie müssen ein [IMailMergeDataSource](../)-Objekt erstellen und zurückgeben, das Aspose.Words den Zugriff auf den OrderDetails‑Datensatz des aktuellen Auftrags ermöglicht.

Wenn dieses Datenquellenobjekt keine Beziehung zur Tabelle mit dem angegebenen Namen hat, müssen Sie ein [IMailMergeDataSource](../)-Objekt zurückgeben, das Zugriff auf alle Datensätze der angegebenen Tabelle bietet.

Wenn eine Tabelle mit dem angegebenen Namen nicht existiert, sollte Ihre Implementierung **null** zurückgeben.

## Siehe auch

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
