---
title: AsposeLlmModel
linktitle: AsposeLlmModel
articleTitle: AsposeLlmModel
second_title: Aspose.Words for .NET
description: AsposeLlmModel constructor. Initializes a new instance of the AsposeLlmModel class for a specified Aspose.LLM preset.
type: docs
weight: 10
url: /net/aspose.words.ai/asposellmmodel/asposellmmodel/
---
## AsposeLlmModel constructor

Initializes a new instance of the [`AsposeLlmModel`](../) class for a specified Aspose.LLM preset.

```csharp
public AsposeLlmModel(string presetName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| presetName | String | The name of the Aspose.LLM preset class that selects the local model family and its runtime, for example "Qwen25Preset". Nothing is loaded or downloaded when this constructor runs. |

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
