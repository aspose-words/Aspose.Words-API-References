---
title: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat yöntemi"
linktitle: "get_UseInvariantCultureNumberFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat yöntemi. C++'ta sayı biçiminin değişmez kültür kullanılarak ayrıştırılıp ayrıştırılmadığını gösteren değeri alır veya ayarlar."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_useinvariantculturenumberformat/
---
## FieldOptions::get_UseInvariantCultureNumberFormat method


Sayı formatının değişmez kültür kullanılarak ayrıştırılıp ayrıştırılmadığını gösteren değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat() const
```

## Açıklamalar


Bu özellik **true** olarak ayarlandığında, sayı biçimi değişmez bir kültürden alınır.

Bu özellik **false** olarak ayarlandığında, sayı biçimi geçerli iş parçacığının kültüründen alınır.

Varsayılan değer **false**'tur.

## Örnekler



Sayıları değişmez kültüre göre nasıl biçimlendireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::Threading::Thread::get_CurrentThread()->set_CurrentCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" = 1234567,89 \\# $#,###,###.##");
field->Update();

// Bazen, alanlar belirli kültürlerde sayılarını doğru biçimlendiremeyebilir.
ASSERT_FALSE(doc->get_FieldOptions()->get_UseInvariantCultureNumberFormat());
ASSERT_EQ(u"$1.234.567,89 ,     ", field->get_Result());

// Bunu düzeltmek için, tüm iş parçacığının kültürünü değiştirebiliriz.
// Bunu düzeltmenin bir başka yolu ise bu bayrağı ayarlamaktır,
// bu, tüm alanların sayı biçimlendirirken değişmez kültürü kullanmasını sağlar.
// Bu yöntem, tüm iş parçacığının kültürünü değiştirmekten kaçınmamızı sağlar.
doc->get_FieldOptions()->set_UseInvariantCultureNumberFormat(true);
field->Update();
ASSERT_EQ(u"$1.234.567,89", field->get_Result());
```

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
