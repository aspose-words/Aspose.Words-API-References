---
title: "Aspose::Words::DocumentBuilder::get_Italic yöntemi"
linktitle: "get_Italic"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_Italic yöntemi. C++'ta yazı tipi italik olarak biçimlendirilmişse true döner."
type: docs
weight: 21000
url: /tr/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


Yazı tipi italik olarak biçimlendirilmişse Doğru.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Örnekler



Bir belge oluşturucu kullanarak, bir posta birleştirme yerine MERGEFIELD'leri veriyle doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Posta birleştirme sırasında veri kaynağındaki aynı ada sahip sütunlardan veri kabul eden bazı MERGEFIELD'leri ekleyin,
// ve ardından onları manuel olarak doldurun.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Ayrıca Bakınız

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
