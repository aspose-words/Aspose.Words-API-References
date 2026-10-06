---
title: AsposeLlmModel.Summarize
linktitle: Summarize
articleTitle: Summarize
second_title: Aspose.Words for .NET
description: AsposeLlmModel Summarize method. Generates a summary of the specified document with options to adjust the length of the summary.
type: docs
weight: 40
url: /net/aspose.words.ai/asposellmmodel/summarize/
---
## Summarize(*[Document](../../../aspose.words/document/), [SummarizeOptions](../../summarizeoptions/)*) {#summarize}

Generates a summary of the specified document, with options to adjust the length of the summary.

```csharp
public override Document Summarize(Document sourceDocument, SummarizeOptions options = null)
```

## Examples

Shows how to summarize documents with a local model, so the content never leaves the machine.

```csharp
// Aspose.LLM is a separate package with its own license, for example:
// new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

// Disposing the model releases the local model and its native resources.
using (AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu"))
{
    Document summary = model.Summarize(firstDoc, new SummarizeOptions { SummaryLength = SummaryLength.Short });
    summary.Save(ArtifactsDir + "AI.AsposeLlmSummarize.One.docx");

    Document combinedSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions { SummaryLength = SummaryLength.Medium });
    combinedSummary.Save(ArtifactsDir + "AI.AsposeLlmSummarize.Multiple.docx");
}
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* class [AsposeLlmModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)

---

## Summarize(*Document[], [SummarizeOptions](../../summarizeoptions/)*) {#summarize_1}

Generates a summary for an array of documents, with options to adjust the length of the summary.

```csharp
public override Document Summarize(Document[] sourceDocuments, SummarizeOptions options = null)
```

## Examples

Shows how to summarize documents with a local model, so the content never leaves the machine.

```csharp
// Aspose.LLM is a separate package with its own license, for example:
// new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

// Disposing the model releases the local model and its native resources.
using (AsposeLlmModel model = new AsposeLlmModel("Qwen25_3BPresetCpu"))
{
    Document summary = model.Summarize(firstDoc, new SummarizeOptions { SummaryLength = SummaryLength.Short });
    summary.Save(ArtifactsDir + "AI.AsposeLlmSummarize.One.docx");

    Document combinedSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions { SummaryLength = SummaryLength.Medium });
    combinedSummary.Save(ArtifactsDir + "AI.AsposeLlmSummarize.Multiple.docx");
}
```

### See Also

* class [Document](../../../aspose.words/document/)
* class [SummarizeOptions](../../summarizeoptions/)
* class [AsposeLlmModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
