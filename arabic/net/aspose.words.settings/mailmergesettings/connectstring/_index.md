---
title: MailMergeSettings.ConnectString
linktitle: ConnectString
articleTitle: ConnectString
second_title: Aspose.Words لـ .NET
description: MailMergeSettings ConnectString ملكية. يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/mailmergesettings/connectstring/
---
## MailMergeSettings.ConnectString property

يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string ConnectString { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ عملية دمج البريد أثناء الاتصال بمصدر بيانات خارجي.

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

// يمكننا إعادة ضبط هذه الإعدادات عن طريق مسحها. بمجرد أن نفعل ذلك ونحفظ المستند،
// لن يقوم Microsoft Word بعد الآن بتنفيذ عملية دمج البريد عندما نستخدمه لتحميل المستند.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### أنظر أيضا

* class [MailMergeSettings](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
