---
title: Odso.TableName
second_title: Справочник по API Aspose.Words для .NET
description: Odso свойство. Указывает конкретный набор данных к которому должен быть подключен источник во внешнем источнике данных. Значение по умолчанию  пустая строка.
type: docs
weight: 80
url: /ru/net/aspose.words.settings/odso/tablename/
---
## Odso.TableName property

Указывает конкретный набор данных, к которому должен быть подключен источник во внешнем источнике данных. Значение по умолчанию — пустая строка.

```csharp
public string TableName { get; set; }
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

* class [Odso](../)
* пространство имен [Aspose.Words.Settings](../../odso/)
* сборка [Aspose.Words](../../../)


