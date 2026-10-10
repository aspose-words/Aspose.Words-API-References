---
title: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks yöntemi"
linktitle: "get_ShowParagraphMarks"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks yöntemi. Paragraf işaretlerinin render edilip edilmediğini gösteren değeri alır veya ayarlar. Varsayılan değer C++'ta false'tur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Paragraf işaretlerinin görüntülenip görüntülenmeyeceğini gösteren değeri alır veya ayarlar. Varsayılan **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Örnekler



Bir oluşturulmuş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bazı paragraflar ekleyin, ardından paragraf işaretlerini etkinleştirerek paragrafların sonlarını gösterin
// belgeyi oluşturduğumuzda pilcrow (¶) sembolüyle.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Ayrıca Bakınız

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
