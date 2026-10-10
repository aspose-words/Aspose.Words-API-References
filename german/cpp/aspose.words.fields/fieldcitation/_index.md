---
title: "Aspose::Words::Fields::FieldCitation class"
linktitle: "FieldCitation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldCitation class. Implementiert das CITATION-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implementiert das CITATION‑Feld. Um mehr zu erfahren, besuchen Sie den [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Ruft einen Wert ab, der dem Wert des **Tag**-Elements einer anderen Quelle entspricht, die in die Zitation aufgenommen werden soll. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Ruft die Sprach-ID ab, die in Verbindung mit dem angegebenen bibliografischen Stil verwendet wird, um die Zitation im Dokument zu formatieren. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_PageNumber](./get_pagenumber/)() | Ruft eine Seitenzahl ab, die mit der Zitation verknüpft ist. |
| [get_Prefix](./get_prefix/)() | Ruft ein Präfix ab, das der Zitation vorangestellt wird. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SourceTag](./get_sourcetag/)() | Ruft einen Wert ab, der dem Wert des **Tag**-Elements der einzufügenden Quelle entspricht. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Suffix](./get_suffix/)() | Ruft ein Suffix ab, das an die Zitation angehängt wird. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Ruft ab, ob die Autoreninformation aus der Zitation unterdrückt wird. |
| [get_SuppressTitle](./get_suppresstitle/)() | Ruft ab, ob die Titelinformation aus der Zitation unterdrückt wird. |
| [get_SuppressYear](./get_suppressyear/)() | Ruft ab, ob die Jahresinformation aus der Zitation unterdrückt wird. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_VolumeNumber](./get_volumenumber/)() | Ruft eine Bandnummer ab, die mit der Zitation verknüpft ist. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Legt einen Wert fest, der dem Wert des **Tag**-Elements einer anderen Quelle entspricht, die in die Zitation aufgenommen werden soll. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Legt die Sprach-ID fest, die in Verbindung mit dem angegebenen bibliografischen Stil verwendet wird, um die Zitation im Dokument zu formatieren. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Legt eine Seitenzahl fest, die mit der Zitation verknüpft ist. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Legt ein Präfix fest, das der Zitation vorangestellt wird. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Setzt einen Wert, der dem Wert des **Tag**-Elements der Quelle entspricht, die eingefügt werden soll. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Setzt ein Suffix, das an das Zitat angehängt wird. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Legt fest, ob die Autoreninformationen im Zitat unterdrückt werden. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Legt fest, ob die Titelinformationen im Zitat unterdrückt werden. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Legt fest, ob die Jahresinformationen im Zitat unterdrückt werden. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Setzt eine Bandnummer, die mit dem Zitat verknüpft ist. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
