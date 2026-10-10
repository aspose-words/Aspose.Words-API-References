---
title: "Aspose::Words::Fields::Field::get_LocaleId metodu"
linktitle: "get_LocaleId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_LocaleId metodu. C++'ta alanın LCID'sini alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.fields/field/get_localeid/
---
## Field::get_LocaleId method


Alan'ın LCID'sini alır veya ayarlar.

```cpp
int32_t Aspose::Words::Fields::Field::get_LocaleId()
```


## Örnekler



Bir alan eklemeyi ve yerel ayarıyla çalışmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir DATE alanı ekleyin ve ardından görüntülenecek tarihi yazdırın.
// İş parçacığınızın mevcut kültürü, tarihin biçimlendirmesini belirler.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE");
std::cout << System::String::Format(u"Today's date, as displayed in the \"{0}\" culture: {1}", System::Globalization::CultureInfo::get_CurrentCulture()->get_EnglishName(), field->get_Result()) << std::endl;

ASSERT_EQ(1033, field->get_LocaleId());

// İş parçacığımızın kültürünü değiştirmek, DATE alanının sonucunu etkileyecektir.
// DATE alanının farklı bir kültürde tarih göstermesini sağlamanın bir başka yolu, LocaleId özelliğini kullanmaktır.
// Bu yöntem, bu etkiyi elde etmek için iş parçacığının kültürünü değiştirmememizi sağlar.
doc->get_FieldOptions()->set_FieldUpdateCultureSource(Aspose::Words::Fields::FieldUpdateCultureSource::FieldCode);
auto de = System::MakeObject<System::Globalization::CultureInfo>(u"de-DE");
field->set_LocaleId(de->get_LCID());
field->Update();

std::cout << System::String::Format(u"Today's date, as displayed according to the \"{0}\" culture: {1}", System::Globalization::CultureInfo::GetCultureInfo(field->get_LocaleId())->get_EnglishName(), field->get_Result()) << std::endl;
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
