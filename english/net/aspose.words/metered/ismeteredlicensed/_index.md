---
title: Metered.IsMeteredLicensed
linktitle: IsMeteredLicensed
articleTitle: IsMeteredLicensed
second_title: Aspose.Words for .NET
description: Discover if your metered method is licensed with IsMetered. Ensure compliance and unlock the benefits of licensed services today!
type: docs
weight: 60
url: /net/aspose.words/metered/ismeteredlicensed/
---
## Metered.IsMeteredLicensed method

Check whether metered is licensed

```csharp
public static bool IsMeteredLicensed()
```

### Return Value

True or false

## Examples

Shows how to activate a Metered license and track credit/consumption.

```csharp
// Create a new Metered license, and then print its usage statistics.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
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
