---
title: "Aspose::Words::Fields::FieldCollection Klasse"
linktitle: "FieldCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldCollection Klasse. Eine Sammlung von Field-Objekten, die die Felder im angegebenen Bereich darstellt. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 23000
url: /de/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Eine Sammlung von [Field](../field/) Objekten, die die Felder im angegebenen Bereich darstellt. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clear](./clear/)() | Entfernt alle Felder dieser Sammlung aus dem Dokument und aus der Sammlung selbst. |
| [get_Count](./get_count/)() | Gibt die Anzahl der Felder in der Sammlung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt ein Feld am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Entfernt das angegebene Feld aus dieser Sammlung und aus dem Dokument. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein Feld am angegebenen Index aus dieser Sammlung und aus dem Dokument. |
| static [Type](./type/)() |  |
## Hinweise


Eine Instanz dieser Sammlung iteriert über Felder, die innerhalb des angegebenen Bereichs beginnen.

Die [FieldCollection](./)-Sammlung besitzt die enthaltenen Felder nicht, sondern ist lediglich eine Auswahl von Feldern.

Die [FieldCollection](./)-Sammlung ist "live", d.h. Änderungen an den Kindknoten des Knotens, von dem sie erstellt wurde, werden sofort in den von den [FieldCollection](./)-Eigenschaften und -Methoden zurückgegebenen Feldern widergespiegelt.

## Beispiele



Zeigt, wie man Felder aus einer Feldsammlung entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Unten sind vier Methoden zum Entfernen von Feldern aus einer Feldsammlung aufgeführt.
// 1 -  Ein Feld erhalten, das sich selbst entfernt:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Die Sammlung erhalten, um ein Feld zu entfernen, das wir ihrer Entfernungs‑Methode übergeben:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Ein Feld aus einer Sammlung an einem Index entfernen:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Alle Felder aus der Sammlung auf einmal entfernen:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
