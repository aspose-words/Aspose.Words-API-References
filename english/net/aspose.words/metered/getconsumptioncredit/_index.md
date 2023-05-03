---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
second_title: Aspose.Words for .NET API Reference
description: Metered GetConsumptionCredit method. Gets consumption credit in C#.
type: docs
weight: 30
url: /net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Gets consumption credit

```csharp
public static decimal GetConsumptionCredit()
```

### Return Value

consumption quantity

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
* namespace [Aspose.Words](../../metered/)
* assembly [Aspose.Words](../../../)
