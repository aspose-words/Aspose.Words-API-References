---
title: ToArray
second_title: Aspose.Words for C++ API Reference
description: Copies all paragraphs from the collection to a new array of paragraphs.
type: docs
weight: 14
url: /cpp/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection::ToArray method


Copies all paragraphs from the collection to a new array of paragraphs.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Paragraph>> Aspose::Words::ParagraphCollection::ToArray()
```


### ReturnValue

An array of paragraphs.

## Examples



Shows how to create an array from a [NodeCollection](../../nodecollection/). 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

ArrayPtr<SharedPtr<Paragraph>> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray();

ASSERT_EQ(22, paras->get_Length());
```


Shows how to use "hot remove" to remove a node during enumeration. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"The first paragraph");
builder->Writeln(u"The second paragraph");
builder->Writeln(u"The third paragraph");
builder->Writeln(u"The fourth paragraph");

// Remove a node from the collection in the middle of an enumeration.
for (SharedPtr<Paragraph> para : doc->get_FirstSection()->get_Body()->get_Paragraphs()->ToArray())
{
    if (para->get_Range()->get_Text().Contains(u"third"))
    {
        para->Remove();
    }
}

ASSERT_FALSE(doc->GetText().Contains(u"The third paragraph"));
```

## See Also

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
