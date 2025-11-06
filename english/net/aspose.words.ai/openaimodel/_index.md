---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AI.OpenAiModel class—your gateway to seamless integration with OpenAI's powerful language models for enhanced document processing.
type: docs
weight: 80
url: /net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

An abstract class representing the integration with OpenAI's large language models within the Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Properties

| Name | Description |
| --- | --- |
| [Timeout](../../aspose.words.ai/aimodel/timeout/) { get; set; } | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| override [Url](../../aspose.words.ai/openaimodel/url/) { get; set; } | Gets or sets a URL of the model. The default value is "https://api.openai.com/". |

## Methods

| Name | Description |
| --- | --- |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| override [Summarize](../../aspose.words.ai/openaimodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
| override [Summarize](../../aspose.words.ai/openaimodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
| override [Translate](../../aspose.words.ai/openaimodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Sets a specified Organization to the model. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Sets a specified Project to the model. |

## Examples

Shows how to use self-hosted AI model based on OpenAiModel.

```csharp
public void SelfHostedModel()
{
    Document doc = new Document(MyDir + "Big document.docx");

    string apiKey = Environment.GetEnvironmentVariable("API_KEY");
    // Use OpenAI generative language models.
    AiModel model = new CustomAiModel().WithApiKey(apiKey);
    model.Url = "https://my.a.com/";

    Document translatedDoc = model.Translate(doc, Language.Russian);
    translatedDoc.Save(ArtifactsDir + "AI.SelfHostedModel.docx");
}

/// <summary>
/// Custom self-hosted AI model.
/// </summary>
internal class CustomAiModel : OpenAiModel
{
    /// <summary>
    /// Gets model name.
    /// </summary>
    protected override string Name
    {
        get { return "my-model-24b"; }
    }
}
```

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
AiModel model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* class [AiModel](../aimodel/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
