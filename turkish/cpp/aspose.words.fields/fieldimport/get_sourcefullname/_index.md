---
title: "Aspose::Words::Fields::FieldImport::get_SourceFullName yöntemi."
linktitle: "get_SourceFullName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldImport::get_SourceFullName yöntemi. C++'de resmin konumunu alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldimport/get_sourcefullname/
---
## FieldImport::get_SourceFullName method


Resmin konumunu alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldImport::get_SourceFullName() override
```


## Örnekler



IMPORT ve INCLUDEPICTURE alanlarını kullanarak görüntülerin nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda, yerel dosya sisteminden bağlanan görüntüleri göstermek için kullanabileceğimiz iki benzer alan türü bulunmaktadır.
// 1 -  INCLUDEPICTURE alanı:
auto fieldIncludePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
fieldIncludePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldIncludePicture->GetFieldCode(), u" INCLUDEPICTURE  .*")->get_Success());

// PNG32.FLT filtresini uygulayın.
fieldIncludePicture->set_GraphicFilter(u"PNG32");
fieldIncludePicture->set_IsLinked(true);
fieldIncludePicture->set_ResizeHorizontally(true);
fieldIncludePicture->set_ResizeVertically(true);

// 2 -  IMPORT alanı:
auto fieldImport = System::ExplicitCast<Aspose::Words::Fields::FieldImport>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldImport, true));
fieldImport->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
fieldImport->set_GraphicFilter(u"PNG32");
fieldImport->set_IsLinked(true);

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(fieldImport->GetFieldCode(), u" IMPORT  .* \\\\c PNG32 \\\\d")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IMPORT.INCLUDEPICTURE.docx");
```

## Ayrıca Bakınız

* Class [FieldImport](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
