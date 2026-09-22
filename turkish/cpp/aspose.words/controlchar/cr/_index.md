---
title: "Aspose::Words::ControlChar::Cr metodu"
linktitle: "Cr"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ControlChar::Cr metodu. Taşıyıcı dönüş karakteri: \"\\x000d\" veya \"\\r\". C++'da ParagraphBreak ile aynı."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Taşıyıcı dönüş karakteri: "\x000d" veya "\r". [ParagraphBreak](../paragraphbreak/) ile aynı.

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Örnekler



Kontrol karakterlerinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// DocumentBuilder ile metin içeren paragraflar ekleyin.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Belgeyi metin biçimine dönüştürmek, kontrol karakterlerinin
// belgenin bazı yapısal öğelerini, örneğin sayfa sonlarını, temsil eder.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// Bir belgeyi dize biçimine dönüştürürken,
// Trim yöntemiyle bazı kontrol karakterlerini atlayabiliriz.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
