---
title: "Aspose::Words::Settings::OdsoFieldMapData class"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::OdsoFieldMapData class. Anger hur en kolumn i den externa datakällan ska mappas till de fördefinierade sammanslagningsfälten i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Anger hur en kolumn i den externa datakällan ska mappas till de fördefinierade sammanslagningsfälten i dokumentet. För att läsa mer, besök dokumentationsartikeln [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Returnerar en djup klon av detta objekt. |
| [get_Column](./get_column/)() const | Anger det nollbaserade indexet för kolumnen i en extern datakälla som ska mappas till det lokala namnet på ett specifikt MERGEFIELD-fält. Standardvärdet är 0. |
| [get_MappedName](./get_mappedname/)() const | Anger det fördefinierade sammanslagningsfältets namn som ska mappas till kolumnnumret som anges av egenskapen [Column](./get_column/) inom denna fältmappning. Standardvärdet är en tom sträng. |
| [get_Name](./get_name/)() const | Anger kolumnnamnet i en extern datakälla för den kolumn vars index anges av egenskapen [Column](./get_column/). Standardvärdet är en tom sträng. |
| [get_Type](./get_type/)() const | Anger om ett givet mail merge-fält har mappats till en kolumn i den angivna externa datakällan eller inte. Standardvärdet är [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Anger det nollbaserade indexet för kolumnen i en extern datakälla som ska mappas till det lokala namnet på ett specifikt MERGEFIELD-fält. Standardvärdet är 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Anger det fördefinierade sammanslagningsfältets namn som ska mappas till kolumnnumret som anges av egenskapen [Column](./get_column/) inom denna fältmappning. Standardvärdet är en tom sträng. |
| [set_Name](./set_name/)(const System::String\&) | Anger kolumnnamnet i en extern datakälla för den kolumn vars index anges av egenskapen [Column](./get_column/). Standardvärdet är en tom sträng. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Anger om ett givet mail merge-fält har mappats till en kolumn i den angivna externa datakällan eller inte. Standardvärdet är [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Anmärkningar


Microsoft Word tillhandahåller några fördefinierade sammanslagningsfältnamn som det låter dig infoga i ett dokument som MERGEFIELD eller använda i fälten ADDRESSBLOCK eller GREETINGLINE. Informationen som anges i [OdsoFieldMapData](./) möjliggör att mappa en kolumn i den externa datakällan till ett enskilt fördefinierat sammanslagningsfält.

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
