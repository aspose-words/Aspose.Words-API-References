---
title: "Aspose::Words::Fields::Field Klasse"
linktitle: "Feld"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field Klasse. Stellt ein Microsoft‑Word‑Dokumentfeld dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fields/field/
---
## Field class


Stellt ein Microsoft Word‑Dokumentfeld dar. Weitere Informationen finden Sie im Dokumentationsartikel.

```cpp
class Field : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](./get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](./get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](./get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](./get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](./get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](./get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](./get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](./get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](./get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](./get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](./get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](./getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](./getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_IsDirty](./set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](./update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](./update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Hinweise


Ein Feld in einem Word-Dokument ist eine komplexe Struktur, die aus mehreren Knoten besteht, die Feldanfang, Feldcode, Feldtrennzeichen, Feldresultat und Feldende umfassen. [Fields](../) können verschachtelt sein, reichhaltige Inhalte enthalten und sich über mehrere Absätze oder Abschnitte in einem Dokument erstrecken. Die [Field](./) Klasse ist ein facade Objekt, das Eigenschaften und Methoden bereitstellt, die die Arbeit mit einem Feld als ein einzelnes Objekt ermöglichen.

Die [Start](./get_start/), [Separator](./get_separator/) und [End](./get_end/) Eigenschaften verweisen jeweils auf die Feldanfang-, Trennzeichen- und Endknoten des Feldes.

Der Inhalt zwischen Feldanfang und Trennzeichen ist der Feldcode. Der Inhalt zwischen dem Feldtrennzeichen und dem Feldende ist das Feldresultat. Der Feldcode besteht typischerweise aus einem oder mehreren [Run](../../aspose.words/run/) Objekten, die Anweisungen spezifizieren. Die verarbeitende Anwendung soll den Feldcode ausführen, um das Feldresultat zu berechnen.

Der Vorgang zur Berechnung von Feldresultaten wird Feldaktualisierung genannt. Aspose.Words kann Feldresultate der meisten Feldtypen exakt auf dieselbe Weise aktualisieren, wie Microsoft Word es tut. Besonders bemerkenswert ist, dass Aspose.Words sogar die Resultate der komplexesten Formelfelder berechnen kann. Um das Feldresultat eines einzelnen Feldes zu berechnen, verwenden Sie die Methode [Update](./update/). Um Felder im gesamten Dokument zu aktualisieren, verwenden Sie [UpdateFields](../../aspose.words/document/updatefields/).

Sie können die Nur-Text-Version des Feldcodes mit der Methode [GetFieldCode()](./getfieldcode/) abrufen. Sie können die Nur-Text-Version des Feldresultats mit der Eigenschaft [Result](./get_result/) abrufen und festlegen. Sowohl der Feldcode als auch das Feldresultat können komplexe Inhalte enthalten, wie verschachtelte Felder, Absätze, Formen, Tabellen, und in diesem Fall möchten Sie möglicherweise direkt mit den Feldknoten arbeiten, wenn Sie mehr Kontrolle benötigen.

Sie erstellen keine Instanzen der [Field](./) Klasse direkt. Um ein neues Feld zu erstellen, verwenden Sie die Methode [InsertField()](../).

## Beispiele



Zeigt, wie man ein Feld mithilfe eines Feldcodes in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
