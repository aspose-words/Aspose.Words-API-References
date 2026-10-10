---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes metodu"
linktitle: "get_IgnoreShapes"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes metodu. Metin içinde şekillerin yok sayılıp sayılmayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da false."
type: docs
weight: 11500
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


Metin içindeki şekilleri yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## Örnekler



Metin değiştirirken şekillerin nasıl yok sayılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
