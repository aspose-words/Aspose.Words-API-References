---
title: Aspose::Words::Markup::SmartTag::SmartTag constructor
linktitle: SmartTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SmartTag::SmartTag constructor. Initializes a new instance of the SmartTag class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


Initializes a new instance of the [SmartTag](../) class.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When you create a new node, you need to specify a document to which the node belongs. A node cannot exist without a document because it depends on the document-wide structures such as lists and styles. Although a node always belongs to a document, a node might or might not be a part of the document tree.

When a node is created, it belongs to a document, but is not yet part of the document tree and [ParentNode](../../../aspose.words/node/get_parentnode/) is null. To insert a node into the document, use the [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) methods on the parent node.

## Examples



Shows how to create smart tags. 
```cpp
void Create()
{
    auto doc = MakeObject<Document>();

    // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
    // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
    auto smartTag = MakeObject<SmartTag>(doc);

    // Smart tags are composite nodes that contain their recognized text in its entirety.
    // Add contents to this smart tag manually.
    smartTag->AppendChild(MakeObject<Run>(doc, u"May 29, 2019"));

    // Microsoft Word may recognize the above contents as being a date.
    // Smart tags use the "Element" property to reflect the type of data they contain.
    smartTag->set_Element(u"date");

    // Some smart tag types process their contents further into custom XML properties.
    smartTag->get_Properties()->Add(MakeObject<CustomXmlProperty>(u"Day", String::Empty, u"29"));
    smartTag->get_Properties()->Add(MakeObject<CustomXmlProperty>(u"Month", String::Empty, u"5"));
    smartTag->get_Properties()->Add(MakeObject<CustomXmlProperty>(u"Year", String::Empty, u"2019"));

    // Set the smart tag's URI to the default value.
    smartTag->set_Uri(u"urn:schemas-microsoft-com:office:smarttags");

    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(smartTag);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u" is a date. "));

    // Create another smart tag for a stock ticker.
    smartTag = MakeObject<SmartTag>(doc);
    smartTag->set_Element(u"stockticker");
    smartTag->set_Uri(u"urn:schemas-microsoft-com:office:smarttags");

    smartTag->AppendChild(MakeObject<Run>(doc, u"MSFT"));

    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(smartTag);
    doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild(MakeObject<Run>(doc, u" is a stock ticker."));

    // Print all the smart tags in our document using a document visitor.
    doc->Accept(MakeObject<ExSmartTag::SmartTagPrinter>());

    // Older versions of Microsoft Word support smart tags.
    doc->Save(ArtifactsDir + u"SmartTag.Create.doc");

    // Use the "RemoveSmartTags" method to remove all smart tags from a document.
    ASSERT_EQ(2, doc->GetChildNodes(NodeType::SmartTag, true)->get_Count());

    doc->RemoveSmartTags();

    ASSERT_EQ(0, doc->GetChildNodes(NodeType::SmartTag, true)->get_Count());
}

class SmartTagPrinter : public DocumentVisitor
{
public:
    VisitorAction VisitSmartTagStart(SharedPtr<SmartTag> smartTag) override
    {
        std::cout << "Smart tag type: " << smartTag->get_Element() << std::endl;
        return VisitorAction::Continue;
    }

    VisitorAction VisitSmartTagEnd(SharedPtr<SmartTag> smartTag) override
    {
        std::cout << "\tContents: \"" << smartTag->ToString(SaveFormat::Text) << "\"" << std::endl;

        if (smartTag->get_Properties()->get_Count() == 0)
        {
            std::cout << "\tContains no properties" << std::endl;
        }
        else
        {
            std::cout << "\tProperties: ";
            auto properties = MakeArray<String>(smartTag->get_Properties()->get_Count());
            int index = 0;

            for (const auto& cxp : System::IterateOver(smartTag->get_Properties()))
            {
                properties[index++] = String::Format(u"\"{0}\" = \"{1}\"", cxp->get_Name(), cxp->get_Value());
            }

            std::cout << String::Join(u", ", properties) << std::endl;
        }

        return VisitorAction::Continue;
    }
};
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
