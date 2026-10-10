---
title: "Aspose::Words::ProtectionType enum"
linktitle: "ProtectionType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ProtectionType enum. C++'ta bir belge için koruma tipi."
type: docs
weight: 111000
url: /tr/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Bir belge için koruma türü.

```cpp
enum class ProtectionType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AllowOnlyComments | 1 | Kullanıcı yalnızca belgede yorumları değiştirebilir. |
| AllowOnlyFormFields | 2 | Kullanıcı yalnızca belgede form alanlarına veri girebilir. |
| AllowOnlyRevisions | 0 | Kullanıcı yalnızca belgeye revizyon işaretleri ekleyebilir. |
| ReadOnly | 3 | Belgeye hiçbir değişiklik yapılmasına izin verilmez. Microsoft Word 2003'ten beri kullanılabilir. |
| NoProtection | -1 | Belge korunmamaktadır. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
