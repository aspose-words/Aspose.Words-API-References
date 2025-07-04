---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words for .NET
description: Effortlessly clear section headers and footers with the ClearHeadersFooters method. Streamline your document layout for a polished look!
type: docs
weight: 120
url: /net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Clears the headers and footers of this section.

```csharp
public void ClearHeadersFooters()
```

## Remarks

The text of all headers and footers is cleared, but [`HeaderFooter`](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.

## Examples

Shows how to clear the contents of all headers and footers in a section.

```csharp
Document doc = new Document();

Assert.That(doc.FirstSection.HeadersFooters.Count, Is.EqualTo(0));

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.That(doc.FirstSection.HeadersFooters.Count, Is.EqualTo(2));

Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim(), Is.EqualTo("This is the primary header."));
Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim(), Is.EqualTo("This is the primary footer."));

// Empty all the headers and footers in this section of all their contents.
// The headers and footers themselves will still be present but will have nothing to display.
doc.FirstSection.ClearHeadersFooters();

Assert.That(doc.FirstSection.HeadersFooters.Count, Is.EqualTo(2));

Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim(), Is.EqualTo(string.Empty));
Assert.That(doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim(), Is.EqualTo(string.Empty));
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Clears the headers and footers of this section.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parameter | Type | Description |
| --- | --- | --- |
| preserveWatermarks | Boolean | True if the watermarks shall not be removed. |

## Remarks

The text of all headers and footers is cleared, but [`HeaderFooter`](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.

## Examples

Shows how to clear the contents of header and footer with or without a watermark.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Add a plain text watermark.
doc.Watermark.SetText("Aspose Watermark");

// Make sure the headers and footers have content.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.That(headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim(), Is.EqualTo("First header"));
Assert.That(headersFooters[HeaderFooterType.HeaderEven].GetText().Trim(), Is.EqualTo("Second header"));
Assert.That(headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim(), Is.EqualTo("Third header"));
Assert.That(headersFooters[HeaderFooterType.FooterFirst].GetText().Trim(), Is.EqualTo("First footer"));
Assert.That(headersFooters[HeaderFooterType.FooterEven].GetText().Trim(), Is.EqualTo("Second footer"));
Assert.That(headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim(), Is.EqualTo("Third footer"));

// Removes all header and footer content except watermarks.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.That(headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim(), Is.EqualTo(""));
Assert.That(headersFooters[HeaderFooterType.HeaderEven].GetText().Trim(), Is.EqualTo(""));
Assert.That(headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim(), Is.EqualTo(""));
Assert.That(headersFooters[HeaderFooterType.FooterFirst].GetText().Trim(), Is.EqualTo(""));
Assert.That(headersFooters[HeaderFooterType.FooterEven].GetText().Trim(), Is.EqualTo(""));
Assert.That(headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim(), Is.EqualTo(""));
Assert.That(doc.Watermark.Type, Is.EqualTo(WatermarkType.Text));

// Removes all header and footer content including watermarks.
doc.FirstSection.ClearHeadersFooters(false);
Assert.That(doc.Watermark.Type, Is.EqualTo(WatermarkType.None));
```

### See Also

* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
