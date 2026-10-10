---
title: "Aspose::Words::Fields::FieldAddressBlock Klasse"
linktitle: "FieldAddressBlock"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAddressBlock Klasse. Implementiert das ADDRESSBLOCK-Feld. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class


Implementiert das ADDRESSBLOCK‑Feld. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAddressBlock : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IFormattableMergeField
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FieldAddressBlock](./fieldaddressblock/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/)() | Ruft den ausgeschlossenen Länder-/Regionsnamen ab oder legt ihn fest. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/)() | Ruft ab, ob die Adresse gemäß dem Land/der Region des Empfängers, wie durch POST*CODE (Universal Postal Union 2006) definiert, formatiert werden soll, oder legt dies fest. |
| [get_IncludeCountryOrRegionName](./get_includecountryorregionname/)() | Ruft ab, ob der Name des Landes/der Region einbezogen werden soll, oder legt dies fest. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LanguageId](./get_languageid/)() | Ruft die Sprach-ID ab, die zur Formatierung der Adresse verwendet wird, oder legt sie fest. |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_NameAndAddressFormat](./get_nameandaddressformat/)() | Ruft den Namen und das Adressformat ab oder legt sie fest. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetFieldNames](./getfieldnames/)() override | Gibt eine Sammlung von Namen der Seriendruckfelder zurück, die von dem Feld verwendet werden. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_ExcludedCountryOrRegionName](./set_excludedcountryorregionname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/). |
| [set_FormatAddressOnCountryOrRegion](./set_formataddressoncountryorregion/)(bool) | Setter für [Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/). |
| [set_IncludeCountryOrRegionName](./set_includecountryorregionname/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldAddressBlock::get_IncludeCountryOrRegionName](./get_includecountryorregionname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldAddressBlock::get_LanguageId](./get_languageid/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NameAndAddressFormat](./set_nameandaddressformat/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat](./get_nameandaddressformat/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
