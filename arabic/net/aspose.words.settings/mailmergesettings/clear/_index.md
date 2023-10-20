---
title: MailMergeSettings.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: MailMergeSettings Clear طريقة. مسح إعدادات دمج البريد بحيث أنه عند حفظ المستند لن يتم حفظ أي إعدادات لدمج البريد وسيصبح مستندًا عاديًا في C#.
type: docs
weight: 180
url: /ar/net/aspose.words.settings/mailmergesettings/clear/
---
## MailMergeSettings.Clear method

مسح إعدادات دمج البريد بحيث أنه عند حفظ المستند، لن يتم حفظ أي إعدادات لدمج البريد وسيصبح مستندًا عاديًا.

```csharp
public void Clear()
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
