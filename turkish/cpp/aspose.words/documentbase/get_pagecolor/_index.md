---
title: "Aspose::Words::DocumentBase::get_PageColor yöntemi"
linktitle: "get_PageColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_PageColor yöntemi. Belgenin sayfa rengini alır veya ayarlar. Bu özellik, C++'ta BackgroundShape'ın daha basit bir sürümüdür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/documentbase/get_pagecolor/
---
## DocumentBase::get_PageColor method


Belgenin sayfa rengini alır veya ayarlar. Bu özellik, [BackgroundShape](../get_backgroundshape/) öğesinin daha basit bir sürümüdür.

```cpp
System::Drawing::Color Aspose::Words::DocumentBase::get_PageColor()
```

## Açıklamalar


Bu özellik, belge için katı bir sayfa rengi belirtmenin basit bir yolunu sağlar. Bu özelliği ayarlamak, uygun bir [BackgroundShape](../get_backgroundshape/) oluşturur ve ayarlar.

Sayfa rengi ayarlanmamışsa (ör. belgede arka plan şekli yoksa) **Empty** döndürür.

## Örnekler



Bir belgenin tüm sayfaları için arka plan renginin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->set_PageColor(System::Drawing::Color::get_LightGray());

doc->Save(get_ArtifactsDir() + u"DocumentBase.SetPageColor.docx");
```

## Ayrıca Bakınız

* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
