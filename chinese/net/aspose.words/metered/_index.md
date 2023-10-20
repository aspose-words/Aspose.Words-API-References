---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Metered 班级. 提供设置计量密钥的方法 在 C#.
type: docs
weight: 4160
url: /zh/net/aspose.words/metered/
---
## Metered class

提供设置计量密钥的方法。

要了解更多信息，请访问[许可和订阅](https://docs.aspose.com/words/net/licensing/)文档文章。

```csharp
public class Metered
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Metered](metered/)() | 初始化此类的新实例。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | 设置计量公钥和私钥。 如果您购买计量许可证，则在启动应用程序时，应该调用此 API，通常，这就足够了。 但是，如果总是无法上传消费数据并且超过24小时，许可证将被设置为评估状态， 为了避免这种情况，您应该定期检查许可证状态，如果是评估状态，请再次调用此接口。 |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | 获取消费积分 |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | 获取消耗文件大小 |

## 例子

在此示例中，将尝试设置计量公钥和私钥

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

展示如何激活计量许可证并跟踪信用/消耗。

```csharp
// 创建新的计量许可证，然后打印其使用统计信息。
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// 使用 Aspose.Words 进行操作，然后再次打印我们的计量统计数据以查看我们花费了多少。
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Aspose 计量许可机制不会每次都将使用数据发送到购买服务器，
// 你需要使用等待。
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
