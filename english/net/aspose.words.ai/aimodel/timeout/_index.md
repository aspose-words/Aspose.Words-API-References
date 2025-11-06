---
title: AiModel.Timeout
linktitle: Timeout
articleTitle: Timeout
second_title: Aspose.Words for .NET
description: Sets how long Aspose.Words waits for AI responses, improving performance and reliability.
type: docs
weight: 20
url: /net/aspose.words.ai/aimodel/timeout/
---
## AiModel.Timeout property

Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).

```csharp
public int Timeout { get; set; }
```

## Examples

Shows how to change model default timeout.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
AiModel model = AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);
// Default value 100000ms.
model.Timeout = 250000;
```

### See Also

* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
