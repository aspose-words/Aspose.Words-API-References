---
title: "Aspose::Words::ParagraphCollection::ToArray yöntemi"
linktitle: "ToArray"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphCollection::ToArray yöntemi. C++'ta koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Koleksiyondaki tüm paragrafları yeni bir paragraf dizisine kopyalar.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

Paragrafların bir dizisi.

## Örnekler



Bir [NodeCollection](../../nodecollection/) üzerinden bir dizi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


\"hot remove\" kullanarak bir düğümü yineleme sırasında kaldırmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Yinelemenin ortasında koleksiyondan bir düğüm kaldırın.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Ayrıca Bakınız

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
