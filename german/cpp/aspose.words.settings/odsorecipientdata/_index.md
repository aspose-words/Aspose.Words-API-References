---
title: "Aspose::Words::Settings::OdsoRecipientData Klasse"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::OdsoRecipientData Klasse. Stellt Informationen über einen einzelnen Datensatz in einer externen Datenquelle dar, der vom Seriendruck ausgeschlossen werden soll. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Stellt Informationen über einen einzelnen Datensatz in einer externen Datenquelle dar, der vom Seriendruck ausgeschlossen werden soll. Weitere Informationen finden Sie im Dokumentationsartikel [Seriendruck und Berichterstellung](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Gibt eine tiefe Kopie dieses Objekts zurück. |
| [get_Active](./get_active/)() const | Gibt an, ob der Datensatz aus der Datenquelle beim Durchführen des Seriendrucks in ein Dokument importiert werden soll. Der Standardwert ist **true**. |
| [get_Column](./get_column/)() const | Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0. |
| [get_Hash](./get_hash/)() const | Stellt den Hashcode für diesen Datensatz dar. Manchmal verwendet Microsoft Word den [Hash](./get_hash/) eines gesamten Datensatzes anstelle eines [UniqueTag](./get_uniquetag/)-Werts. Der Standardwert ist 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. Der Standardwert ist **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Gibt an, ob der Datensatz aus der Datenquelle beim Durchführen des Seriendrucks in ein Dokument importiert werden soll. Der Standardwert ist **true**. |
| [set_Column](./set_column/)(int32_t) | Gibt die Spalte in der Datenquelle an, die eindeutige Daten für den aktuellen Datensatz enthält. Der Standardwert ist 0. |
| [set_Hash](./set_hash/)(int32_t) | Stellt den Hashcode für diesen Datensatz dar. Manchmal verwendet Microsoft Word den [Hash](./get_hash/) eines gesamten Datensatzes anstelle eines [UniqueTag](./get_uniquetag/)-Werts. Der Standardwert ist 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Gibt den Inhalt eines bestimmten Datensatzes in der Spalte mit eindeutigen Daten an. Der Standardwert ist **null**. |
| static [Type](./type/)() |  |
## Hinweise


Wenn ein Datensatz in ein zusammengeführtes Dokument eingefügt werden soll, werden keine Informationen zu diesem Datensatz benötigt. Wenn jedoch ein bestimmter Datensatz nicht in ein zusammengeführtes Dokument eingefügt werden soll, muss der Wert des eindeutigen Schlüssels für diesen Datensatz in der [UniqueTag](./get_uniquetag/)-Eigenschaft dieses Objekts gespeichert werden, um diesen Ausschluss anzuzeigen.
## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
