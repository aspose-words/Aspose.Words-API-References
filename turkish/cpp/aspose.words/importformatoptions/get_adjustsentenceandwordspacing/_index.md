---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing yöntemi"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing yöntemi. Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'ta false'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Örnekler



Cümle ve kelime aralığını otomatik olarak nasıl ayarlayacağınızı gösterir.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## Ayrıca Bakınız

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
