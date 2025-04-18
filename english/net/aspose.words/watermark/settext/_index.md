---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words for .NET
description: Enhance your documents with our Watermark SetText method. Easily add customizable text watermarks for a professional touch!
type: docs
weight: 40
url: /net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

Adds Text watermark into the document.

```csharp
public void SetText(string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | String | Text that is displayed as a watermark. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throws when the text length is out of range or the text contains only whitespaces. |
| ArgumentNullException | Throws when the text is `null`. |

## Remarks

The text length must be in the range from 1 to 200 inclusive. The text cannot be `null` or contain only whitespaces.

## Examples

Shows how to create a text watermark.

```csharp
Document doc = new Document();

// Add a plain text watermark.
doc.Watermark.SetText("Aspose Watermark");

// If we wish to edit the text formatting using it as a watermark,
// we can do so by passing a TextWatermarkOptions object when creating the watermark.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// We can remove a watermark from a document like this.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### See Also

* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Adds Text watermark into the document.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | String | Text that is displayed as a watermark. |
| options | TextWatermarkOptions | Defines additional options for the text watermark. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throws when the text length is out of range or the text contain only whitespaces. |
| ArgumentNullException | Throws when the text is `null`. |

## Remarks

The text length must be in the range from 1 to 200 inclusive. The text cannot be `null` or contain only whitespaces.

If [`TextWatermarkOptions`](../../textwatermarkoptions/) is `null`, the watermark will be set with default options.

## Examples

Shows how to create a text watermark.

```csharp
Document doc = new Document();

// Add a plain text watermark.
doc.Watermark.SetText("Aspose Watermark");

// If we wish to edit the text formatting using it as a watermark,
// we can do so by passing a TextWatermarkOptions object when creating the watermark.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// We can remove a watermark from a document like this.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### See Also

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
