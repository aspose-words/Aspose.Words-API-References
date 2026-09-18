---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::Odso class. Gibt die Einstellungen des Office Data Source Object (ODSO) für eine Seriendruck‑Datenquelle an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.settings/odso/
---
## Odso class


Gibt die Einstellungen des Office Data Source Object (ODSO) für eine Seriendruck‑Datenquelle an. Weitere Informationen finden Sie im Dokumentationsartikel [Seriendruck und Berichterstellung](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Gibt das Zeichen an, das als Spaltentrennzeichen interpretiert wird, um Spalten in externen Datenquellen zu trennen. Der Standardwert ist 0, was bedeutet, dass kein Spaltentrennzeichen definiert ist. |
| [get_DataSource](./get_datasource/)() const | Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument für den Seriendruck verbunden werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [get_DataSourceType](./get_datasourcetype/)() const | Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO‑Verbindungsinformationen für diesen Seriendruck verbunden werden soll. Der Standardwert ist [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Ruft eine Sammlung von Objekten ab, die festlegen, wie Spalten aus der externen Datenquelle den vordefinierten Seriendruckfeldnamen im Dokument zugeordnet werden. Dieses Objekt ist niemals **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Gibt an, dass eine Host‑Anwendung die erste Datenzeile in der angegebenen externen Datenquelle als Kopfzeile behandelt, die die Namen jeder Spalte in der Datenquelle enthält. Der Standardwert ist **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Ruft eine Sammlung von Objekten ab, die die Aufnahme/Ausschluss einzelner Datensätze im Seriendruck festlegen. Dieses Objekt ist niemals **null**. |
| [get_TableName](./get_tablename/)() const | Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Gibt die Universal Data Link (UDL)-Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Setter für [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Gibt den Speicherort der externen Datenquelle an, die mit einem Dokument für den Seriendruck verbunden werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Setter für [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Legt eine Sammlung von Objekten fest, die angeben, wie Spalten aus der externen Datenquelle auf die vordefinierten Merge-Feldnamen im Dokument abgebildet werden. Dieses Objekt ist niemals **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Setter für [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Legt eine Sammlung von Objekten fest, die den Ein- bzw. Ausschluss einzelner Datensätze im Seriendruck angeben. Dieses Objekt ist niemals **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Gibt den konkreten Datensatz an, mit dem eine Quelle innerhalb einer externen Datenquelle verbunden werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Gibt die Universal Data Link (UDL)-Verbindungszeichenfolge an, die zum Verbinden mit einer externen Datenquelle verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| static [Type](./type/)() |  |
## Hinweise


ODSO scheint die „neue“ Methode zu sein, die neueren Microsoft‑Word‑Versionen bevorzugen, wenn sie bestimmte Arten von Datenquellen für ein Seriendruckdokument angeben. ODSO ist wahrscheinlich erstmals in Microsoft Word 2000 aufgetaucht.

Die Verwendung von ODSO ist schlecht dokumentiert, und der beste Weg, zu lernen, wie man die Eigenschaften dieses Objekts nutzt, besteht darin, ein Dokument mit einer gewünschten Datenquelle manuell in Microsoft Word zu erstellen und dieses Dokument anschließend mit Aspose.Words zu öffnen und die Eigenschaften der [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/)‑ und [Odso](../mailmergesettings/get_odso/)‑Objekte zu untersuchen. Dies ist ein guter Ansatz, wenn Sie beispielsweise lernen möchten, wie man eine Datenquelle programmgesteuert konfiguriert.

Sie müssen normalerweise keine Objekte dieser Klasse direkt erstellen, da ODSO‑Einstellungen stets über die [Odso](../mailmergesettings/get_odso/)‑Eigenschaft verfügbar sind.

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
