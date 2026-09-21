---
title: "Aspose::Words::ParagraphCollection::ToArray metod"
linktitle: "ToArray"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphCollection::ToArray metod. Kopierar alla stycken från samlingen till en ny array av stycken i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Kopierar alla stycken från samlingen till en ny array av stycken.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

En array av stycken.

## Exempel



Visar hur man skapar en array från en [NodeCollection](../../nodecollection/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Visar hur man använder "hot remove" för att ta bort en nod under enumerering.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Ta bort en nod från samlingen mitt i en enumerering.
for (System::SharedPtr<Aspose::Words::Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## Se även

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
