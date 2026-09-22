---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes yöntemi"
linktitle: "get_IsInKilobytes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes yöntemi. C++'ta dosya boyutunun kilobayt olarak gösterilip gösterilmeyeceğini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldfilesize/get_isinkilobytes/
---
## FieldFileSize::get_IsInKilobytes method


Dosya boyutunun kilobayt cinsinden gösterilip gösterilmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes()
```


## Örnekler



Bir FILESIZE alanı ile belgenin dosya boyutunun nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Aşağıda üç farklı ölçü birimi bulunmaktadır
// FILESIZE alanlarının belgenin dosya boyutunu gösterebileceği birimler.
// 1 -  Bayt:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobayt:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabayt:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Microsoft Word'de düzenleme yaparken bu alanların değerlerini güncellemek için,
// önce değişiklikleri kaydetmeli, ardından bu alanları manuel olarak güncellemeliyiz.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Ayrıca Bakınız

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
