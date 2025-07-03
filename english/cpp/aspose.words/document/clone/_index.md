---
title: Aspose::Words::Document::Clone method
linktitle: Clone
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::Clone method. Performs a deep copy of the Document in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/document/clone/
---
## Document::Clone method


Performs a deep copy of the [Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

The cloned document.

## Examples



Shows how to deep clone a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// Cloning will produce a new document with the same contents as the original,
// but with a unique copy of each of the original document's nodes.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## See Also

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
