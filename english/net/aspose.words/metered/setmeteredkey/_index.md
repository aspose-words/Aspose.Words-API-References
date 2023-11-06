---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words for .NET
description: Metered SetMeteredKey method. Sets metered public and private key. If you purchase metered license when start application this API should be called normally this is enough. However if always fail to upload consumption data and exceed 24 hours the license will be set to evaluation status to avoid such case you should regularly check the license status if it is evaluation status call this API again in C#.
type: docs
weight: 30
url: /net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Sets metered public and private key. If you purchase metered license, when start application, this API should be called, normally, this is enough. However, if always fail to upload consumption data and exceed 24 hours, the license will be set to evaluation status, to avoid such case, you should regularly check the license status, if it is evaluation status, call this API again.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parameter | Type | Description |
| --- | --- | --- |
| publicKey | String | public key |
| privateKey | String | private key |

## Examples

Shows how to activate a Metered license and track credit/consumption.

```csharp
// Create a new Metered license, and then print its usage statistics.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Operate using Aspose.Words, and then print our metered stats again to see how much we spent.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing mechanism does not send the usage data to purchase server every time,
// you need to use waiting.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### See Also

* class [Metered](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
