---
title: "Aspose::Words::Fields::FieldFormat::get_GeneralFormats Methode"
linktitle: "get_GeneralFormats"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldFormat::get_GeneralFormats Methode. Gibt eine Sammlung von allgemeinen Formaten zurück, die auf ein numerisches, Text‑ oder beliebiges Feldresultat angewendet werden. Entspricht den \\*‑Schaltern in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldformat/get_generalformats/
---
## FieldFormat::get_GeneralFormats method


Liest eine Sammlung allgemeiner Formate, die auf das Ergebnis eines numerischen, Text‑ oder beliebigen Feldes angewendet werden. Entspricht den \*‑Schaltern.

```cpp
System::SharedPtr<Aspose::Words::Fields::GeneralFormatCollection> Aspose::Words::Fields::FieldFormat::get_GeneralFormats()
```


## Beispiele



Zeigt, wie Feldresultate formatiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie den Document Builder, um ein Feld einzufügen, das ein Ergebnis ohne angewendetes Format anzeigt.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Wir können ein Format auf das Ergebnis eines Feldes anwenden, indem wir die Eigenschaften des Feldes verwenden.
// Im Folgenden sind drei Arten von Formaten aufgeführt, die wir auf das Ergebnis eines Feldes anwenden können.
// 1 -  Numerisches Format:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Datums-/Uhrzeitformat:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Allgemeines Format:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Wir können unsere Formate entfernen, um das Ergebnis des Feldes in seine ursprüngliche Form zurückzusetzen.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Siehe auch

* Class [GeneralFormatCollection](../../generalformatcollection/)
* Class [FieldFormat](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
