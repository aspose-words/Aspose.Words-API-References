---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: Discover the ParagraphFormat Bidi property to easily control right-to-left text formatting for enhanced readability and improved document layout.
type: docs
weight: 50
url: /net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Gets or sets whether this is a right-to-left paragraph.

```csharp
public bool Bidi { get; set; }
```

## Remarks

When `true`, the runs and other inline objects in this paragraph are laid out right to left.

## Examples

Shows how to detect plaintext document text direction.

```csharp
// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
// the direction of every paragraph of text that Aspose.Words loads from plaintext.
// Each paragraph's "Bidi" property will store its direction.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Detect Hebrew text as right-to-left.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Detect English text as right-to-left.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
// but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
// The following field will display ".1", the RTL equivalent of list number "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Set the horizontal text alignment for every paragraph in the document to RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
// Otherwise, they will display "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
