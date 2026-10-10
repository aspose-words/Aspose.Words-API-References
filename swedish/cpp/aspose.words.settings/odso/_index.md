---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::Odso class. Anger inställningarna för Office Data Source Object (ODSO) för en kopplad datakälla för brevfletning. Läs mer genom att besöka dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.settings/odso/
---
## Odso class


Anger inställningarna för Office Data Source Object (ODSO) för en mail merge-datakälla. För att läsa mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Returnerar en djup klon av detta objekt. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Anger tecknet som ska tolkas som kolumnavgränsare som används för att separera kolumner i externa datakällor. Standardvärdet är 0 vilket betyder att ingen kolumnavgränsare är definierad. |
| [get_DataSource](./get_datasource/)() const | Anger platsen för den externa datakällan som ska anslutas till ett dokument för att utföra brevfletning. Standardvärdet är en tom sträng. |
| [get_DataSourceType](./get_datasourcetype/)() const | Anger typen av den externa datakällan som ska anslutas som en del av ODSO-anslutningsinformationen för denna brevfletning. Standardvärdet är [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Hämtar en samling objekt som anger hur kolumner från den externa datakällan mappas till de fördefinierade sammanslagningsfältens namn i dokumentet. Detta objekt är aldrig **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Anger att ett värdprogram ska behandla den första raden med data i den angivna externa datakällan som en rubrikrad som innehåller namnen på varje kolumn i datakällan. Standardvärdet är **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Hämtar en samling objekt som anger inkludering/uteslutning av enskilda poster i brevfletningen. Detta objekt är aldrig **null**. |
| [get_TableName](./get_tablename/)() const | Anger den specifika datamängden som en källa ska anslutas till inom en extern datakälla. Standardvärdet är en tom sträng. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Anger Universal Data Link (UDL)-anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Sättare för [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Anger platsen för den externa datakällan som ska anslutas till ett dokument för att utföra brevfletning. Standardvärdet är en tom sträng. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Sättare för [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Ställer in en samling objekt som anger hur kolumner från den externa datakällan mappas till de fördefinierade sammanslagningsfältens namn i dokumentet. Detta objekt är aldrig **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Inställare för [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Anger en samling objekt som specificerar inkludering/uteslutning av enskilda poster i kopplad utskrift. Detta objekt är aldrig **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Anger den specifika datamängden som en källa ska anslutas till inom en extern datakälla. Standardvärdet är en tom sträng. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Anger Universal Data Link (UDL)-anslutningssträngen som används för att ansluta till en extern datakälla. Standardvärdet är en tom sträng. |
| static [Type](./type/)() |  |
## Anmärkningar


ODSO verkar vara det "nya" sättet som de nyare versionerna av Microsoft Word föredrar att använda när man specificerar vissa typer av datakällor för ett kopplat utskriftsdokument. ODSO introducerades sannolikt först i Microsoft Word 2000.

Användningen av ODSO är dåligt dokumenterad och det bästa sättet att lära sig hur man använder egenskaperna för detta objekt är att skapa ett dokument med en önskad datakälla manuellt i Microsoft Word och sedan öppna det dokumentet med Aspose.Words och undersöka egenskaperna för [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) och [Odso](../mailmergesettings/get_odso/) objekten. Detta är ett bra tillvägagångssätt om du vill lära dig hur du programatiskt konfigurerar en datakälla, till exempel.

Du behöver normalt inte skapa objekt av denna klass direkt eftersom ODSO-inställningar alltid är tillgängliga via egenskapen [Odso](../mailmergesettings/get_odso/).

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
