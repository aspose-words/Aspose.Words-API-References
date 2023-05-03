---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
second_title: Aspose.Words for .NET API Reference
description: StructuredDocumentTag method. Sets the symbol used to represent the unchecked state of a check box content control in C#.
type: docs
weight: 370
url: /net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Sets the symbol used to represent the unchecked state of a check box content control.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | Int32 | The character code for the specified symbol. |
| fontName | String | The name of the font that contains the symbol. |

## Remarks

Accessing this method will only work for Checkbox SDT types.

For all other SDT types exception will occur.

## Examples

Show how to create a structured document tag in the form of a check box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../structureddocumenttag/)
* assembly [Aspose.Words](../../../)
