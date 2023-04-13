---
title: SmartTag Class
linktitle: SmartTag
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Markup.SmartTag class. This element specifies the presence of a smart tag around one or more inline structures runs images fieldsetc. within a paragraph in C#.
type: docs
weight: 3880
url: /net/aspose.words.markup/smarttag/
---
## SmartTag class

This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class SmartTag : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [SmartTag](smarttag/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initializes a new instance of the `SmartTag` class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [Element](../../aspose.words.markup/smarttag/element/) { get; set; } | Specifies the name of the smart tag within the document. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype/) { get; } | Returns SmartTag. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Properties](../../aspose.words.markup/smarttag/properties/) { get; } | A collection of the smart tag properties. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [Uri](../../aspose.words.markup/smarttag/uri/) { get; set; } | Specifies the namespace URI of the smart tag. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all `SmartTag` descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../../aspose.words/node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

`SmartTag` can be a child of a [`Paragraph`](../../aspose.words/paragraph/) or another `SmartTag` node.

The complete list of child nodes that can occur inside a smart tag consists of [`BookmarkStart`](../../aspose.words/bookmarkstart/), [`BookmarkEnd`](../../aspose.words/bookmarkend/), [`FieldStart`](../../aspose.words.fields/fieldstart/), [`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/), [`FormField`](../../aspose.words.fields/formfield/), [`Comment`](../../aspose.words/comment/), [`Footnote`](../../aspose.words.notes/footnote/), [`Run`](../../aspose.words/run/), [`SpecialChar`](../../aspose.words/specialchar/), [`Shape`](../../aspose.words.drawing/shape/), [`GroupShape`](../../aspose.words.drawing/groupshape/), [`CommentRangeStart`](../../aspose.words/commentrangestart/), [`CommentRangeEnd`](../../aspose.words/commentrangeend/), `SmartTag`.

## Examples

Shows how to create smart tags.

```csharp
public void Create()
{
    Document doc = new Document();

    // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
    // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
    SmartTag smartTag = new SmartTag(doc);

    // Smart tags are composite nodes that contain their recognized text in its entirety.
    // Add contents to this smart tag manually.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word may recognize the above contents as being a date.
    // Smart tags use the "Element" property to reflect the type of data they contain.
    smartTag.Element = "date";

    // Some smart tag types process their contents further into custom XML properties.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Set the smart tag's URI to the default value.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Create another smart tag for a stock ticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Print all the smart tags in our document using a document visitor.
    doc.Accept(new SmartTagPrinter());

    // Older versions of Microsoft Word support smart tags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Use the "RemoveSmartTags" method to remove all smart tags from a document.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Prints visited smart tags and their contents.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Called when a SmartTag node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when the visiting of a SmartTag node is ended.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### See Also

* class [CompositeNode](../../aspose.words/compositenode/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
