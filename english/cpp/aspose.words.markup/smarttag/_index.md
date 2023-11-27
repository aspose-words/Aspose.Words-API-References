---
title: Aspose::Words::Markup::SmartTag class
linktitle: SmartTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SmartTag class. This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. To learn more, visit the  documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.markup/smarttag/
---
## SmartTag class


This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class SmartTag : public Aspose::Words::CompositeNode,
                 public Aspose::Words::Markup::IMarkupNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Element](./get_element/)() const | Specifies the name of the smart tag within the document. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [SmartTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Properties](./get_properties/)() const | A collection of the smart tag properties. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [get_Uri](./get_uri/)() const | Specifies the namespace URI of the smart tag. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](./) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Element](./set_element/)(const System::String\&) | Setter for [Aspose::Words::Markup::SmartTag::get_Element](./get_element/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Uri](./set_uri/)(const System::String\&) | Setter for [Aspose::Words::Markup::SmartTag::get_Uri](./get_uri/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initializes a new instance of the [SmartTag](./) class. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

The complete list of child nodes that can occur inside a smart tag consists of [BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [CommentRangeStart](../../aspose.words/commentrangestart/), [CommentRangeEnd](../../aspose.words/commentrangeend/), [SmartTag](./).

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

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
