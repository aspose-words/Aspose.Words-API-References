---
title: Class HeaderFooter
second_title: Aspose.Words for .NET API Reference
description: Represents a container for the header or footer text of a section.
type: docs
weight: 2940
url: /net/aspose.words/headerfooter/
---
## HeaderFooter class

Represents a container for the header or footer text of a section.

To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/net/working-with-headers-and-footers/) documentation article.

```csharp
public class HeaderFooter : Story
```

## Constructors

| Name | Description |
| --- | --- |
| [HeaderFooter](headerfooter/)(DocumentBase, HeaderFooterType) | Creates a new header or footer of the specified type. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Gets the first paragraph in the story. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [HeaderFooterType](../../aspose.words/headerfooter/headerfootertype/) { get; } | Gets the type of this header/footer. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [IsHeader](../../aspose.words/headerfooter/isheader/) { get; } | True if this `HeaderFooter` object is a header. |
| [IsLinkedToPrevious](../../aspose.words/headerfooter/islinkedtoprevious/) { get; set; } | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Gets the last paragraph in the story. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/headerfooter/nodetype/) { get; } | Returns HeaderFooter. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Gets a collection of paragraphs that are immediate children of the story. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentSection](../../aspose.words/headerfooter/parentsection/) { get; } | Gets the parent section of this story. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Gets the type of this story. |
| [Tables](../../aspose.words/story/tables/) { get; } | Gets a collection of tables that are immediate children of the story. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/headerfooter/accept/)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | A shortcut method that creates a [`Paragraph`](../paragraph/) object with optional text and appends it to the end of this object. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserved for system use. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Deletes all shapes from the text of this story. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

`HeaderFooter` can contain [`Paragraph`](../paragraph/) and [`Table`](../../aspose.words.tables/table/) child nodes.

`HeaderFooter` is a section-level node and can only be a child of [`Section`](../section/). There can only be one `HeaderFooter` of each [`HeaderFooterType`](./headerfootertype/) in a [`Section`](../section/).

If [`Section`](../section/) does not have a `HeaderFooter` of a specific type or the `HeaderFooter` has no child nodes, this header/footer is considered linked to the header/footer of the same type of the previous section in Microsoft Word.

When `HeaderFooter` contains at least one [`Paragraph`](../paragraph/), it is no longer considered linked to previous in Microsoft Word.

## Examples

Shows how to replace text in a document's footer.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Shows how to delete all footers from a document.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
foreach (Section section in doc.OfType<Section>())
{
    // There are three kinds of footer and header types.
    // 1 -  The "First" header/footer, which only appears on the first page of a section.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

    // 3 -  The "Even" header/footer, which appears on even pages. 
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Shows how to create a header and a footer.

```csharp
Document doc = new Document();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### See Also

* class [Story](../story/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
