---
title: MailMergeSettings.AddressFieldName
linktitle: AddressFieldName
articleTitle: AddressFieldName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMergeSettings AddressFieldName, чтобы легко указать столбец адреса электронной почты в источниках данных, гарантируя бесперебойное объединение писем.
type: docs
weight: 30
url: /ru/net/aspose.words.settings/mailmergesettings/addressfieldname/
---
## MailMergeSettings.AddressFieldName property

Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка.

```csharp
public string AddressFieldName { get; set; }
```

## Примеры

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
// Microsoft Word больше не будет выполнять слияние почты, когда мы используем его для загрузки документа.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Смотрите также

* class [MailMergeSettings](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
