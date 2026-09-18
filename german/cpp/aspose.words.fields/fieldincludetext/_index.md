---
title: "Aspose::Words::Fields::FieldIncludeText class"
linktitle: "FieldIncludeText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIncludeText class. Implementiert das INCLUDETEXT-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 58000
url: /de/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implementiert das INCLUDETEXT-Feld. Weitere Informationen finden Sie im [Arbeiten mit Feldern](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Ermittelt den Namen des Lesezeichens im einzuschließenden Dokument. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_Encoding](./get_encoding/)() | Ermittelt die auf die Daten in der referenzierten Datei angewendete Kodierung. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_LockFields](./get_lockfields/)() override | Ermittelt, ob Felder im eingeschlossenen Dokument daran gehindert werden sollen, aktualisiert zu werden. |
| [get_MimeType](./get_mimetype/)() | Ermittelt den MIME-Typ der referenzierten Datei. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Ermittelt die Namespace-Zuordnungen für XPath-Abfragen. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SourceFullName](./get_sourcefullname/)() override | Ermittelt den Speicherort des Dokuments mittels einer IRI. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_TextConverter](./get_textconverter/)() override | Ermittelt den Namen des Textkonverters für das Format der eingeschlossenen Datei. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_XPath](./get_xpath/)() override | Ermittelt XPath für den gewünschten Teil der XML-Datei. |
| [get_XslTransformation](./get_xsltransformation/)() override | Ermittelt den Speicherort der XSL-Transformation zum Formatieren von XML-Daten. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Legt den Namen des Lesezeichens im einzuschließenden Dokument fest. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Legt die auf die Daten in der referenzierten Datei angewendete Kodierung fest. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Legt fest, ob Felder im eingeschlossenen Dokument vor einer Aktualisierung geschützt werden sollen. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Legt den MIME-Typ der referenzierten Datei fest. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Legt die Namespace-Zuordnungen für XPath-Abfragen fest. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Legt den Speicherort des Dokuments mittels einer IRI fest. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Legt den Namen des Textkonverters für das Format der eingeschlossenen Datei fest. |
| [set_XPath](./set_xpath/)(const System::String\&) | Legt XPath für den gewünschten Teil der XML-Datei fest. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Legt den Speicherort der XSL-Transformation zum Formatieren von XML-Daten fest. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
