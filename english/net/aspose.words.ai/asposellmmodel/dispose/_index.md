---
title: AsposeLlmModel.Dispose
linktitle: Dispose
articleTitle: Dispose
second_title: Aspose.Words for .NET
description: AsposeLlmModel Dispose method. Releases the underlying Aspose.LLM model and its native resources.
type: docs
weight: 30
url: /net/aspose.words.ai/asposellmmodel/dispose/
---
## AsposeLlmModel.Dispose method

Releases the underlying Aspose.LLM model and its native resources.

```csharp
public void Dispose()
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

* class [AsposeLlmModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
