---
title: Odso.TableName
second_title: Aspose.Words for .NET API 参考
description: Odso 财产. 指定源应在外部数据源内连接到的特定数据集 默认值为空字符串
type: docs
weight: 80
url: /zh/net/aspose.words.settings/odso/tablename/
---
## Odso.TableName property

指定源应在外部数据源内连接到的特定数据集。 默认值为空字符串。

```csharp
public string TableName { get; set; }
```

### 例子

演示如何在连接到外部数据源时执行邮件合并。

```csharp
Document doc = new Document(MyDir + "Odso data.docx");
MailMergeSettings settings = doc.MailMergeSettings;

Console.WriteLine($"Connection string:\n\t{settings.ConnectString}");
Console.WriteLine($"Mail merge docs as attachment:\n\t{settings.MailAsAttachment}");
Console.WriteLine($"Mail merge doc e-mail subject:\n\t{settings.MailSubject}");
Console.WriteLine($"Column that contains e-mail addresses:\n\t{settings.AddressFieldName}");
Console.WriteLine($"Active record:\n\t{settings.ActiveRecord}");

Odso odso = settings.Odso;

Console.WriteLine($"File will connect to data source located in:\n\t\"{odso.DataSource}\"");
Console.WriteLine($"Source type:\n\t{odso.DataSourceType}");
Console.WriteLine($"UDL connection string:\n\t{odso.UdlConnectString}");
Console.WriteLine($"Table:\n\t{odso.TableName}");
Console.WriteLine($"Query:\n\t{doc.MailMergeSettings.Query}");

// 我们可以通过清除它们来重置这些设置。一旦我们这样做并保存文档，
// 当我们使用 Microsoft Word 加载文档时，它将不再执行邮件合并。
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### 也可以看看

* class [Odso](../)
* 命名空间 [Aspose.Words.Settings](../../odso/)
* 部件 [Aspose.Words](../../../)


