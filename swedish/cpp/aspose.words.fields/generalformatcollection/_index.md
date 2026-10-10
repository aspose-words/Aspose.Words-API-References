---
title: "Aspose::Words::Fields::GeneralFormatCollection klass"
linktitle: "GeneralFormatCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::GeneralFormatCollection klass. Representerar en typad samling av allmänna format. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 114000
url: /sv/cpp/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class


Representerar en typad samling av allmänna format.

```cpp
class GeneralFormatCollection : public System::Collections::Generic::IEnumerable<Aspose::Words::Fields::GeneralFormat>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(Aspose::Words::Fields::GeneralFormat) | Lägger till ett allmänt format i samlingen. |
| [get_Count](./get_count/)() | Hämtar det totala antalet objekt i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett allmänt format på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(Aspose::Words::Fields::GeneralFormat) | Tar bort alla förekomster av det angivna allmänna formatet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort en förekomst av ett allmänt format på det angivna indexet. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man formaterar fältresultat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Använd en dokumentbyggare för att infoga ett fält som visar ett resultat utan någon formatering tillämpad.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Vi kan tillämpa en formatering på ett fälts resultat med hjälp av fältets egenskaper.
// Nedan är tre typer av formateringar som vi kan tillämpa på ett fälts resultat.
// 1 -  Numeriskt format:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Datum/tid-format:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Allmänt format:
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

// Vi kan ta bort våra format för att återställa fältets resultat till dess ursprungliga form.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
