---
title: MailMergeSettings.MailAsAttachment
second_title: Справочник по API Aspose.Words для .NET
description: MailMergeSettings свойство. Указывает что документы созданные во время операции слияния должны отправляться по электронной почте в виде вложения а не в виде  а не тела фактического сообщения электронной почты. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 120
url: /ru/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

Указывает, что документы, созданные во время операции слияния, должны отправляться по электронной почте в виде вложения, а не в виде , а не тела фактического сообщения электронной почты. Значение по умолчанию`ЛОЖЬ` .

```csharp
public bool MailAsAttachment { get; set; }
```

### Примеры

Показывает, как выполнить слияние почты при подключении к внешнему источнику данных.

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

// Мы можем сбросить эти настройки, очистив их. Как только мы это сделаем и сохраним документ,
// Microsoft Word больше не будет выполнять слияние, когда мы используем его для загрузки документа.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Смотрите также

* class [MailMergeSettings](../)
* пространство имен [Aspose.Words.Settings](../../mailmergesettings/)
* сборка [Aspose.Words](../../../)


