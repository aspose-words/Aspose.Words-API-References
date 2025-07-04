---
title: Aspose::Words::RevisionCollection::AcceptAll method
linktitle: AcceptAll
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::RevisionCollection::AcceptAll method. Accepts all revisions in this collection in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Accepts all revisions in this collection.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Examples



Shows how to compare documents. 
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Comparing documents with revisions will throw an exception.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// After the comparison, the original document will gain a new revision
// for every element that is different in the edited document.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Accepting these revisions will transform the original document into the edited document.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## See Also

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
