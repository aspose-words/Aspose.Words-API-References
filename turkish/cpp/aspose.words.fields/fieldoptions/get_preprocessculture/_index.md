---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture yöntemi"
linktitle: "get_PreProcessCulture"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture yöntemi. C++'ta alan değerlerini ön işleme tabi tutmak için kültürü alır veya ayarlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Alan değerlerini ön işlemek için kültürü alır veya ayarlar.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Açıklamalar


Şu anda bu özellik yalnızca [FieldDocProperty](../../fielddocproperty/) alanının değerini etkiler.

Varsayılan değer **null**'dır. Bu özellik **null** olarak ayarlandığında, [FieldDocProperty](../../fielddocproperty/) alanının değeri, [FieldUpdateCultureSource](../get_fieldupdateculturesource/) özelliği tarafından kontrol edilen kültürle ön işleme tabi tutulur.

## Örnekler



Ön işleme kültürünün nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bazı alanların görüntülenen değerlerini hangi kültüre göre biçimlendireceğini belirlemek için kültürü ayarlayın.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// DOCPROPERTY alanı, sonucunu ön işleme kültürüne göre biçimlendirilmiş olarak gösterir
// Almanca olarak ayarladık. Alan, tarih/saat bilgisini "dd.mm.yyyy hh:mm" biçiminde gösterecek.
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Değişmez kültüre geçtikten sonra, DOCPROPERTY alanı "mm/dd/yyyy hh:mm" biçimini kullanacaktır.
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
