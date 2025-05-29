---
title: MailMergeSettings.AddressFieldName
linktitle: AddressFieldName
articleTitle: AddressFieldName
second_title: Aspose.Words for .NET
description: 发现 MailMergeSettings AddressFieldName 属性，轻松指定数据源中的电子邮件地址列，确保无缝电子邮件合并。
type: docs
weight: 30
url: /zh/net/aspose.words.settings/mailmergesettings/addressfieldname/
---
## MailMergeSettings.AddressFieldName property

指定数据源中包含电子邮件地址的列。默认值为空字符串。

```csharp
public string AddressFieldName { get; set; }
```

## 例子

显示如何在连接到外部数据源时执行邮件合并。

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

// 我们可以通过清除这些设置来重置它们。清除后，保存文档，
// 当我们使用 Microsoft Word 加载文档时，它将不再执行邮件合并。
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### 也可以看看

* class [MailMergeSettings](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
