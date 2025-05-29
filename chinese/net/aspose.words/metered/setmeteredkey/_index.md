---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words for .NET
description: 使用 SetMeteredKey 方法轻松管理您的计量许可证。确保数据无缝上传，并通过定期检查避免评估状态。
type: docs
weight: 30
url: /zh/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

设置计量公钥和私钥。 如果您购买了计量许可证，则在启动应用程序时应调用此 API，通常这就足够了。 但是，如果始终无法上传消费数据并且超过 24 小时，许可证将被设置为评估状态， 为避免这种情况，您应该定期检查许可证状态，如果是评估状态，请再次调用此 API。

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| publicKey | String | 公钥 |
| privateKey | String | 私钥 |

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
