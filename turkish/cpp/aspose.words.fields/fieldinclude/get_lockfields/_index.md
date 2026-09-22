---
title: "Aspose::Words::Fields::FieldInclude::get_LockFields yöntemi"
linktitle: "get_LockFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldInclude::get_LockFields yöntemi. C++'ta dahil edilen belgede alanların güncellenmesini önleyip önlemeyeceğini alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldinclude/get_lockfields/
---
## FieldInclude::get_LockFields method


Dahil edilen belgede alanların güncellenmesini önleyip önlemeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldInclude::get_LockFields() override
```


## Örnekler



INCLUDE alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerel dosya sistemindeki başka bir belgenin bir bölümünü içe aktarmak için bir INCLUDE alanı kullanabiliriz.
// Bu alanla başvurduğumuz diğer belgedeki yer imi, bu içe aktarılan bölümü içerir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Ayrıca Bakınız

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
