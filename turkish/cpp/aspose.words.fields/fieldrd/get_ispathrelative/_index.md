---
title: "Aspose::Words::Fields::FieldRD::get_IsPathRelative yöntemi"
linktitle: "get_IsPathRelative"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldRD::get_IsPathRelative yöntemi. C++'ta yolun geçerli belgeye göre göreli olup olmadığını alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldrd/get_ispathrelative/
---
## FieldRD::get_IsPathRelative method


Yolun geçerli belgeye göre göreli olup olmadığını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldRD::get_IsPathRelative()
```


## Örnekler



Diğer belgelerdeki başlıklardan içindekiler tablosu girdileri oluşturmak için RD alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir belge oluşturucu kullanarak bir içindekiler tablosu ekleyin,
// ve ardından sonraki sayfada içindekiler tablosu için bir giriş ekleyin.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// FileName özelliğinde başka bir yerel dosya sistemi belgesine başvuran bir RD alanı ekleyin.
// İçindekiler tablosu artık başvurulan belgedeki tüm başlıkları tablosu için giriş olarak kabul edecek.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// RD alanının başvurduğu belgeyi oluşturun ve bir başlık ekleyin.
// Bu başlık, ilk belgemizdeki TOC alanında bir giriş olarak görünecek.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## Ayrıca Bakınız

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
