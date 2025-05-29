---
title: Metered.IsMeteredLicensed
linktitle: IsMeteredLicensed
articleTitle: IsMeteredLicensed
second_title: Aspose.Words for .NET
description: 了解您的计量方法是否已获得 IsMetered 许可。立即确保合规性并解锁许可服务的优势！
type: docs
weight: 60
url: /zh/net/aspose.words/metered/ismeteredlicensed/
---
## Metered.IsMeteredLicensed method

检查计量是否已获得许可

```csharp
public static bool IsMeteredLicensed()
```

### 返回值

对还是错

## 例子

展示如何激活计量许可证并跟踪信用/消费。

```csharp
// 创建一个新的计量许可证，然后打印其使用情况统计信息。
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// 使用 Aspose.Words 进行操作，然后再次打印我们的计量统计数据，以查看我们花了多少钱。
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing 机制不会每次都将使用数据发送到购买服务器，
// 您需要使用等待。
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### 也可以看看

* class [Metered](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
