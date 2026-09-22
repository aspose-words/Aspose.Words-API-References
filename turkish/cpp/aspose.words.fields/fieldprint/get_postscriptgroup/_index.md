---
title: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup metodu"
linktitle: "get_PostScriptGroup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldPrint::get_PostScriptGroup metodu. C++'da PostScript talimatlarının çalıştığı çizim dikdörtgenini alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldprint/get_postscriptgroup/
---
## FieldPrint::get_PostScriptGroup method


PostScript talimatlarının çalıştığı çizim dikdörtgenini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldPrint::get_PostScriptGroup()
```


## Örnekler



PRINT alanı eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"My paragraph");

// PRINT alanı, yazıcıya talimatlar gönderebilir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrint>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPrint, true));

// Yazıcının talimatları uygulayacağı alanı ayarlayın.
// Bu durumda, PRINT alanımızı içeren paragraf olacaktır.
field->set_PostScriptGroup(u"para");

// Belgemizi yazdırmak için PostScript destekleyen bir yazıcı kullandığımızda,
// bu komut, "field.PostScriptGroup" içinde belirttiğimiz tüm alanı beyaz yapar.
field->set_PrinterInstructions(u"erasepage");

ASSERT_EQ(u" PRINT  erasepage \\p para", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.PRINT.docx");
```

## Ayrıca Bakınız

* Class [FieldPrint](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
