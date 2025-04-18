---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words for .NET
description: Create powerful structured documents effortlessly with the StructuredDocumentTag constructor. Initialize new instances for enhanced organization and clarity.
type: docs
weight: 10
url: /net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Initializes a new instance of the **Structured document tag** class.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| type | SdtType | Type of SDT node. |
| level | MarkupLevel | Level of SDT node within the document. |

## Remarks

The following types of SDT can be created:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

## Examples

Show how to create a structured document tag in the form of a check box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### See Also

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
