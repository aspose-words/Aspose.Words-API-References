---
title: Metered.GetConsumptionQuantity
second_title: Aspose.Words for .NET API 参考
description: Metered 方法. 获取消耗文件大小
type: docs
weight: 40
url: /zh/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

获取消耗文件大小

```csharp
public static decimal GetConsumptionQuantity()
```

### 返回值

消费数量

### 例子

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

* class [Metered](../)
* 命名空间 [Aspose.Words](../../metered/)
* 部件 [Aspose.Words](../../../)


