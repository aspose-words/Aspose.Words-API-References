---
title: "Aspose::Words::Fields::FieldOptions::get_FileName yöntemi"
linktitle: "get_FileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldOptions::get_FileName yöntemi. Belgenin dosya adını C++'ta alır veya ayarlar."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Belgenin dosya adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Açıklamalar


Bu özellik, [FieldFileName](../../fieldfilename/) alanı tarafından, [OriginalFileName](../../../aspose.words/document/get_originalfilename/) özelliğine göre daha yüksek öncelikle kullanılır.

## Örnekler



[FieldOptions](../) kullanarak FILENAME alanı için varsayılan değeri nasıl geçersiz kılacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Bu FILENAME alanı, yüklediğimiz belgenin yerel sistem dosya adını gösterecektir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Varsayılan olarak, FILENAME alanı dosyanın adını gösterir, ancak tam yerel dosya sistemi yolunu göstermez.
// Tam dosya yolunu göstermesi için bir bayrak ayarlayabiliriz.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Bu özellik için bir değer de ayarlayabiliriz
// FILENAME alanının gösterdiği değeri geçersiz kılmak.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Ayrıca Bakınız

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
