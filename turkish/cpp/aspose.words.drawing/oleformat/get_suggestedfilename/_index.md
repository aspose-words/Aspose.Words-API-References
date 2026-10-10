---
title: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metodu"
linktitle: "get_SuggestedFileName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::get_SuggestedFileName metodu. C++'da mevcut gömülü nesneyi bir dosyaya kaydetmek isterseniz önerilen dosya adını alır."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.drawing/oleformat/get_suggestedfilename/
---
## OleFormat::get_SuggestedFileName method


Mevcut gömülü nesne için bir dosyaya kaydetmek isterseniz önerilen dosya adını alır.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SuggestedFileName()
```


## Örnekler



Bir OLE nesnesinin önerilen dosya adını nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE shape.rtf");

auto oleShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// OLE nesneleri önerilen bir dosya adı ve uzantı sağlayabilir,
// bu, nesnenin içeriğini yerel dosya sisteminde bir dosyaya kaydederken kullanabiliriz.
System::String suggestedFileName = oleShape->get_OleFormat()->get_SuggestedFileName();

ASSERT_EQ(u"CSV.csv", suggestedFileName);

{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + suggestedFileName, System::IO::FileMode::Create);
    oleShape->get_OleFormat()->Save(fileStream);
}
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
