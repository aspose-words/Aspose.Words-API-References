---
title: "Aspose::Words::Section::get_ProtectedForForms yöntemi"
linktitle: "get_ProtectedForForms"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::get_ProtectedForForms yöntemi. Bölüm formlara korumalıysa doğru döner. Bir bölüm formlara korumalı olduğunda, kullanıcılar Microsoft Word'de yalnızca form alanlarındaki metni seçebilir ve değiştirebilir C++'ta."
type: docs
weight: 14000
url: /tr/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Bölüm formlar için korumalıysa True. Bölüm formlar için korumalı olduğunda, kullanıcılar Microsoft Word'de yalnızca form alanlarındaki metni seçebilir ve değiştirebilir.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


## Örnekler



Bir bölüm için korumayı nasıl kapatacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygula.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapat.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// Bu çıktı belgesinde, ilk bölümü serbestçe düzenleyebileceğiz,
// ve yalnızca ikinci bölmedeki form alanının içeriğini düzenleyebileceğiz.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Ayrıca Bakınız

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
