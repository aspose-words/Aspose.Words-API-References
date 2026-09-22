---
title: "Aspose::Words::Fields::GeneralFormatCollection sınıfı"
linktitle: "GeneralFormatCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::GeneralFormatCollection sınıfı. Genel formatların tiplenmiş bir koleksiyonunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 114000
url: /tr/cpp/aspose.words.fields/generalformatcollection/
---
## GeneralFormatCollection class


Genel formatların tiplenmiş bir koleksiyonunu temsil eder. Daha fazla bilgi edinmek için [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokümantasyon makalesini ziyaret edin.

```cpp
class GeneralFormatCollection : public System::Collections::Generic::IEnumerable<Aspose::Words::Fields::GeneralFormat>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(Aspose::Words::Fields::GeneralFormat) | Koleksiyona bir genel format ekler. |
| [get_Count](./get_count/)() | Koleksiyondaki öğelerin toplam sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir genel formatı alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(Aspose::Words::Fields::GeneralFormat) | Belirtilen genel formatın koleksiyondaki tüm örneklerini kaldırır. |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir genel format örneğini kaldırır. |
| static [Type](./type/)() |  |

## Örnekler



Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Biçim uygulanmamış bir sonuç gösteren bir alan eklemek için belge oluşturucusunu kullanın.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Bir alanın özelliklerini kullanarak alanın sonucuna bir biçim uygulayabiliriz.
// Aşağıda bir alanın sonucuna uygulayabileceğimiz üç biçim türü bulunmaktadır.
// 1 -  Sayısal biçim:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Tarih/saat biçimi:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Genel biçim:
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

// Biçimlerimizi kaldırarak alanın sonucunu orijinal haline geri döndürebiliriz.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
