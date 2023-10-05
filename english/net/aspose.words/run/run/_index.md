---
title: Run
linktitle: Run
articleTitle: Run
second_title: Aspose.Words for .NET
description: Run constructor. Initializes a new instance of the Run class in C#.
type: docs
weight: 10
url: /net/aspose.words/run/run/
---
## Run(*[DocumentBase](../../documentbase/)*) {#constructor}

Initializes a new instance of the [`Run`](../) class.

```csharp
public Run(DocumentBase doc)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |

## Remarks

When [`Run`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`Run`](../) to the document use [`InsertAfter`](../../compositenode/insertafter/) or [`InsertBefore`](../../compositenode/insertbefore/) on the paragraph where you want the run inserted.

### See Also

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## Run(*[DocumentBase](../../documentbase/), string*) {#constructor_1}

Initializes a new instance of the **Run** class.

```csharp
public Run(DocumentBase doc, string text)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| text | String | The text of the run. |

## Remarks

When [`Run`](../) is created, it belongs to the specified document, but is not yet part of the document and [`ParentNode`](../../node/parentnode/) is `null`.

To append [`Run`](../) to the document use [`InsertAfter`](../../compositenode/insertafter/) or [`InsertBefore`](../../compositenode/insertbefore/) on the paragraph where you want the run inserted.

## Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### See Also

* class [DocumentBase](../../documentbase/)
* class [Run](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
