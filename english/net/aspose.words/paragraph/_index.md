---
title: "Paragraph"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 4090
url: /net/aspose.words/paragraph/
---
## Paragraph class

Represents a paragraph of text.

```csharp
public class Paragraph : CompositeNode
```

## Public Members

| Name | Description |
| --- | --- |
| [Paragraph](paragraph)(…) | Initializes a new instance of the Paragraph class. |
| [BreakIsStyleSeparator](breakisstyleseparator) { get; } | True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles. |
| [FrameFormat](frameformat) { get; } | Provides access to the paragraph formatting properties. |
| [IsDeleteRevision](isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsEndOfCell](isendofcell) { get; } | True if this paragraph is the last paragraph in a [`Cell`](../../aspose.words.tables/cell); false otherwise. |
| [IsEndOfDocument](isendofdocument) { get; } | True if this paragraph is the last paragraph in the last section of the document. |
| [IsEndOfHeaderFooter](isendofheaderfooter) { get; } | True if this paragraph is the last paragraph in the HeaderFooter (main text story) of a Section; false otherwise. |
| [IsEndOfSection](isendofsection) { get; } | True if this paragraph is the last paragraph in the Body (main text story) of a Section; false otherwise. |
| [IsFormatRevision](isformatrevision) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInCell](isincell) { get; } | True if this paragraph is an immediate child of [`Cell`](../../aspose.words.tables/cell); false otherwise. |
| [IsInsertRevision](isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsListItem](islistitem) { get; } | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [IsMoveFromRevision](ismovefromrevision) { get; } | Returns true if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](ismovetorevision) { get; } | Returns true if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [ListFormat](listformat) { get; } | Provides access to the list formatting properties of the paragraph. |
| [ListLabel](listlabel) { get; } | Gets a [`ListLabel`](./listlabel) object that provides access to list numbering value and formatting for this paragraph. |
| override [NodeType](nodetype) { get; } | Returns NodeType.Paragraph. |
| [ParagraphBreakFont](paragraphbreakfont) { get; } | Provides access to the font formatting of the paragraph break character. |
| [ParagraphFormat](paragraphformat) { get; } | Provides access to the paragraph formatting properties. |
| [ParentSection](parentsection) { get; } | Retrieves the parent [`Section`](../section) of the paragraph. |
| [ParentStory](parentstory) { get; } | Retrieves the parent section-level story that can be [`Body`](../body) or [`HeaderFooter`](../headerfooter). |
| [Runs](runs) { get; } | Provides access to the typed collection of pieces of text inside the paragraph. |
| override [Accept](accept)(…) | Accepts a visitor. |
| [AppendField](appendfield)(…) | Appends a field to this paragraph. (3 methods) |
| [GetEffectiveTabStops](geteffectivetabstops)() | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
| override [GetText](gettext)() | Gets the text of this paragraph including the end of paragraph character. |
| [InsertField](insertfield)(…) | Inserts a field into this paragraph. (3 methods) |
| [JoinRunsWithSameFormatting](joinrunswithsameformatting)() | Joins runs with the same formatting in the paragraph. |

### Remarks

[`Paragraph`](../paragraph) is a block-level node and can be a child of classes derived from [`Story`](../story) or [`InlineStory`](../inlinestory).[`Paragraph`](../paragraph) can contain any number of inline-level nodes and bookmarks.The complete list of child nodes that can occur inside a paragraph consists of [`BookmarkStart`](../bookmarkstart), [`BookmarkEnd`](../bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart), [`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend), [`FormField`](../../aspose.words.fields/formfield), [`Comment`](../comment), [`Footnote`](../../aspose.words.notes/footnote), [`Run`](../run), [`SpecialChar`](../specialchar), [`Shape`](../../aspose.words.drawing/shape), [`GroupShape`](../../aspose.words.drawing/groupshape), [`SmartTag`](../../aspose.words.markup/smarttag).A valid paragraph in Microsoft Word always ends with a paragraph break character and a minimal valid paragraph consists just of a paragraph break. The Paragraph class automatically appends the appropriate paragraph break character at the end and this character is not part of the child nodes of the Paragraph, therefore a Paragraph can be empty.Do not include the end of paragraph [`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak) or end of cell [`ControlChar.Cell`](../controlchar/cell) characters inside the text of the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.

### Examples

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

* class [CompositeNode](../compositenode)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
