---
title: Body
second_title: Aspose.Words for .NET API Reference
description: Represents a container for the main text of a section.
type: docs
weight: 20
url: /net/aspose.words/body/
---
## Body class

Represents a container for the main text of a section.

```csharp
public class Body : Story
```

## Constructors

| Name | Description |
| --- | --- |
| [Body](body)(DocumentBase) | Initializes a new instance of the **Body** class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Gets the first paragraph in the story. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns true as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Gets the last paragraph in the story. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | Returns **NodeType.Body**. |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Gets a collection of paragraphs that are immediate children of the story. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Gets the parent section of this story. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Gets the type of this story. |
| [Tables](../../aspose.words/story/tables/) { get; } | Gets a collection of tables that are immediate children of the story. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(string) | A shortcut method that creates a [`Paragraph`](../paragraph/) object with optional text and appends it to the end of this object. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserved for system use. IXPathNavigable. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Deletes all shapes from the text of this story. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
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
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selects the first Node that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

**Body** can contain **Paragraph** and **Table** child nodes.

**Body** is a section-level node and can only be a child of **Section**. There can only be one **Body** in a **Section**.

A minimal valid **Body** needs to contain at least one **Paragraph**.

## Examples

Shows how to construct an Aspose.Words document by hand.

```csharp
Document doc = new Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
Section section = new Section(doc);
doc.AppendChild(section);

// Set some page setup properties for the section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
Body body = new Body(doc);
section.AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### See Also

* class [Story](../story/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
