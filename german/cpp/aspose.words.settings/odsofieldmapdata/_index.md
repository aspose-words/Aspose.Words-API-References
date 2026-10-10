---
title: "Aspose::Words::Settings::OdsoFieldMapData‑Klasse"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::OdsoFieldMapData‑Klasse. Gibt an, wie eine Spalte in der externen Datenquelle auf die vordefinierten Merge‑Felder im Dokument abgebildet werden soll. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Gibt an, wie eine Spalte in der externen Datenquelle den vordefinierten Seriendruckfeldern im Dokument zugeordnet wird. Weitere Informationen finden Sie im Dokumentationsartikel [Seriendruck und Berichterstellung](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [get_Column](./get_column/)() const | Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. Der Standardwert ist 0. |
| [get_MappedName](./get_mappedname/)() const | Gibt den vordefinierten Namen des Zusammenführungsfeldes an, der der durch die Eigenschaft [Column](./get_column/) angegebenen Spaltennummer in dieser Feldzuordnung zugeordnet werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [get_Name](./get_name/)() const | Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [Column](./get_column/) festgelegt ist. Der Standardwert ist eine leere Zeichenfolge. |
| [get_Type](./get_type/)() const | Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert ist [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Gibt den nullbasierten Index der Spalte in einer externen Datenquelle an, der dem lokalen Namen eines bestimmten MERGEFIELD-Feldes zugeordnet werden soll. Der Standardwert ist 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Gibt den vordefinierten Namen des Zusammenführungsfeldes an, der der durch die Eigenschaft [Column](./get_column/) angegebenen Spaltennummer in dieser Feldzuordnung zugeordnet werden soll. Der Standardwert ist eine leere Zeichenfolge. |
| [set_Name](./set_name/)(const System::String\&) | Gibt den Spaltennamen in einer externen Datenquelle für die Spalte an, deren Index durch die Eigenschaft [Column](./get_column/) festgelegt ist. Der Standardwert ist eine leere Zeichenfolge. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Gibt an, ob ein bestimmtes Seriendruckfeld einer Spalte in der angegebenen externen Datenquelle zugeordnet wurde oder nicht. Der Standardwert ist [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Hinweise


Microsoft Word stellt einige vordefinierte Namen für Seriendruckfelder bereit, die in ein Dokument als MERGEFIELD eingefügt oder in den Feldern ADDRESSBLOCK oder GREETINGLINE verwendet werden können. Die in [OdsoFieldMapData](./) angegebenen Informationen ermöglichen es, eine Spalte in der externen Datenquelle einem einzelnen vordefinierten Seriendruckfeld zuzuordnen.

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
