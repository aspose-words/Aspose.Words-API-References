---
title: GoogleAiModel
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words for .NET
description: GoogleAiModel constructor. Initializes a new instance of GoogleAiModel class.
type: docs
weight: 10
url: /net/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel(*string*) {#constructor}

Initializes a new instance of [`GoogleAiModel`](../) class.

```csharp
public GoogleAiModel(string name)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the model. For example, gemini-2.5-flash. |

## Examples

Shows how to use google AI model.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

Document doc = new Document(MyDir + "Big document.docx");
SummarizeOptions summarizeOptions = new SummarizeOptions() { SummaryLength = SummaryLength.VeryShort };
Document summary = model.Summarize(doc, summarizeOptions);
```

### See Also

* class [GoogleAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)

---

## GoogleAiModel(*string, string*) {#constructor_1}

Initializes a new instance of [`GoogleAiModel`](../) class.

```csharp
public GoogleAiModel(string name, string apiKey)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the model. For example, gemini-2.5-flash. |
| apiKey | String | The API key to use the Gemini API. Please refer to https://ai.google.dev/gemini-api/docs/api-key for details. |

## Examples

Shows how to use google AI model.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

Document doc = new Document(MyDir + "Big document.docx");
SummarizeOptions summarizeOptions = new SummarizeOptions() { SummaryLength = SummaryLength.VeryShort };
Document summary = model.Summarize(doc, summarizeOptions);
```

### See Also

* class [GoogleAiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
