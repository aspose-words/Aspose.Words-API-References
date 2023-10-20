---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: 用于 .NET 的 Aspose.Words
description: Metered SetMeteredKey 方法. 设置计量公钥和私钥 如果购买计量许可证在启动应用程序时应该调用此API正常情况下这就足够了 但是如果总是上传消费数据失败超过24小时License会被设置为评估状态 为了避免这种情况你应该定期检查License状态如果是评估状态再次调用这个API 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

设置计量公钥和私钥。 如果购买计量许可证，在启动应用程序时，应该调用此API，正常情况下，这就足够了。 但是，如果总是上传消费数据失败，超过24小时，License会被设置为评估状态， 为了避免这种情况，你应该定期检查License状态，如果是评估状态，再次调用这个API。

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| publicKey | String | 公钥 |
| privateKey | String | 私钥 |

## 例子

显示如何激活计量许可证和跟踪信用/消耗。

```csharp
// 创建一个新的计量许可证，然后打印其使用统计信息。
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// 使用 Aspose.Words 操作，然后再次打印我们的计量统计数据，看看我们花了多少钱。
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose Metered Licensing 机制不会每次都将使用数据发送到购买服务器，
// 你需要使用等待。
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### 也可以看看

* class [Metered](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
