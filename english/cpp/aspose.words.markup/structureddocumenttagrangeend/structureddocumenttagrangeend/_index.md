---
title: Aspose::Words::Markup::StructuredDocumentTagRangeEnd::StructuredDocumentTagRangeEnd constructor
linktitle: StructuredDocumentTagRangeEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeEnd::StructuredDocumentTagRangeEnd constructor. Initializes a new instance of the Structured document tag range end class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.markup/structureddocumenttagrangeend/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd::StructuredDocumentTagRangeEnd constructor


Initializes a new instance of the **Structured document tag range end** class.

```cpp
Aspose::Words::Markup::StructuredDocumentTagRangeEnd::StructuredDocumentTagRangeEnd(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| id | int32_t | Identifier of the corresponding structured document tag range start. |

## Examples



Shows how to create/remove structured document tag and its content. 
```cpp
void SdtRangeExtendedMethods()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->Writeln(u"StructuredDocumentTag element");

    SharedPtr<StructuredDocumentTagRangeStart> rangeStart;
    InsertStructuredDocumentTagRanges(doc, rangeStart);

    // Removes ranged structured document tag, but keeps content inside.
    rangeStart->RemoveSelfOnly();

    rangeStart = System::DynamicCast<StructuredDocumentTagRangeStart>(doc->GetChild(NodeType::StructuredDocumentTagRangeStart, 0, false));
    ASPOSE_ASSERT_EQ(nullptr, rangeStart);

    auto rangeEnd = System::DynamicCast<StructuredDocumentTagRangeEnd>(doc->GetChild(NodeType::StructuredDocumentTagRangeEnd, 0, false));

    ASPOSE_ASSERT_EQ(nullptr, rangeEnd);
    ASSERT_EQ(u"StructuredDocumentTag element", doc->GetText().Trim());

    InsertStructuredDocumentTagRanges(doc, rangeStart);

    SharedPtr<Node> paragraphNode = rangeStart->LINQ_LastOrDefault();
    ASPOSE_ASSERT_EQ(u"StructuredDocumentTag element",
                     paragraphNode != nullptr ? System::ObjectExt::Box<String>(paragraphNode->GetText().Trim()) : nullptr);

    // Removes ranged structured document tag and content inside.
    rangeStart->RemoveAllChildren();

    paragraphNode = rangeStart->LINQ_LastOrDefault();
    ASPOSE_ASSERT_EQ(nullptr, paragraphNode != nullptr ? System::ObjectExt::Box<String>(paragraphNode->GetText()) : nullptr);
}

void InsertStructuredDocumentTagRanges(SharedPtr<Document> doc, SharedPtr<StructuredDocumentTagRangeStart>& rangeStart)
{
    rangeStart = MakeObject<StructuredDocumentTagRangeStart>(doc, SdtType::PlainText);
    auto rangeEnd = MakeObject<StructuredDocumentTagRangeEnd>(doc, rangeStart->get_Id());

    doc->get_FirstSection()->get_Body()->InsertBefore(rangeStart, doc->get_FirstSection()->get_Body()->get_FirstParagraph());
    doc->get_LastSection()->get_Body()->InsertAfter(rangeEnd, doc->get_FirstSection()->get_Body()->get_FirstParagraph());
}
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [StructuredDocumentTagRangeEnd](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
