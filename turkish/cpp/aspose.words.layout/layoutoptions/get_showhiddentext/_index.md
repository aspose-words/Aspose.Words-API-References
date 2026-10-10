---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText yöntemi"
linktitle: "get_ShowHiddenText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText yöntemi. Belgede gizli metnin render edilip edilmediğini gösteren değeri alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Belgedeki gizli metnin görüntülenip görüntülenmeyeceğini gösteren değeri alır veya ayarlar. Varsayılan **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Örnekler



Bir oluşturulmuş çıktı belgesinde metnin nasıl gizleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gizli metni ekleyin, ardından bunu oluşturulmuş bir belgeden çıkarıp çıkarmak istemediğinizi belirtin.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Ayrıca Bakınız

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
