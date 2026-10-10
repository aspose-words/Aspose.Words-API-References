---
title: "Aspose::Words::DocumentBuilder::get_Underline method"
linktitle: "get_Underline"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_Underline yöntemi. Mevcut yazı tipi için alt çizgi tipini C++'da alır/ayarlar."
type: docs
weight: 26000
url: /tr/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Geçerli yazı tipi için alt çizgi tipini alır/ayarlar.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Örnekler



Bir belge oluşturucu tarafından eklenen metnin nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Oluşturucu, mevcut paragrafına ve sonradan eklediği yeni metne biçimlendirme uygular.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## Ayrıca Bakınız

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
