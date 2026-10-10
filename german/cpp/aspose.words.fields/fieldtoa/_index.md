---
title: "Aspose::Words::Fields::FieldToa Klasse"
linktitle: "FieldToa"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldToa Klasse. Implementiert das TOA-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 104000
url: /de/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implementiert das TOA-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Ermittelt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_EntryCategory](./get_entrycategory/)() | Ermittelt die ganzzahlige Kategorie für in der Tabelle enthaltene Einträge. |
| [get_EntrySeparator](./get_entryseparator/)() | Ermittelt die Zeichenfolge, die verwendet wird, um einen Eintrag im Verzeichnis der Autoritäten und seine Seitenzahl zu trennen. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Ermittelt die Zeichenfolge, die verwendet wird, um zwei Seitenzahlen in einer Seitenzahlenliste zu trennen. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Ermittelt die Zeichenfolge, die verwendet wird, um den Anfang und das Ende eines Seitenbereichs zu trennen. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Ermittelt, ob die Formatierung des Eintragstextes im Dokument aus dem Eintrag im Verzeichnis der Autoritäten entfernt werden soll. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SequenceName](./get_sequencename/)() | Ermittelt den Namen einer Sequenz, deren Nummer mit der Seitenzahl angegeben wird. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Ermittelt die Zeichenfolge, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_UseHeading](./get_useheading/)() | Ermittelt, ob die Kategorienüberschrift für die Einträge in einem Verzeichnis der Autoritäten aufgenommen werden soll. |
| [get_UsePassim](./get_usepassim/)() | Ermittelt, ob fünf oder mehr verschiedene Seitenverweise auf dieselbe Quelle durch "passim" ersetzt werden sollen, was verwendet wird, um anzuzeigen, dass ein Wort oder Abschnitt häufig in der zitierten Arbeit vorkommt. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setzt den Namen des Lesezeichens, das den Teil des Dokuments markiert, der zum Erstellen der Tabelle verwendet wird. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Setzt die ganzzahlige Kategorie für in der Tabelle enthaltene Einträge. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Legt die Zeichenfolge fest, die verwendet wird, um einen Eintrag im Verzeichnis der Autoritäten und seine Seitenzahl zu trennen. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Legt die Zeichenfolge fest, die verwendet wird, um zwei Seitenzahlen in einer Seitenzahlenliste zu trennen. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Legt die Zeichenfolge fest, die verwendet wird, um den Anfang und das Ende eines Seitenbereichs zu trennen. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Legt fest, ob die Formatierung des Eintragstextes im Dokument aus dem Eintrag im Verzeichnis der Autoritäten entfernt werden soll. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Legt den Namen einer Sequenz fest, deren Nummer mit der Seitenzahl enthalten ist. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Legt die Zeichenfolge fest, die verwendet wird, um Sequenznummern und Seitenzahlen zu trennen. |
| [set_UseHeading](./set_useheading/)(bool) | Legt fest, ob die Kategorienüberschrift für die Einträge im Verzeichnis der Autoritäten eingeschlossen werden soll. |
| [set_UsePassim](./set_usepassim/)(bool) | Legt fest, ob fünf oder mehr verschiedene Seitenverweise auf dieselbe Autorität durch \"passim\" ersetzt werden sollen, was verwendet wird, um anzuzeigen, dass ein Wort oder Abschnitt häufig im zitierten Werk vorkommt. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
