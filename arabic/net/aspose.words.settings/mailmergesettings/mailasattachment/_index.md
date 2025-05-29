---
title: MailMergeSettings.MailAsAttachment
linktitle: MailAsAttachment
articleTitle: MailAsAttachment
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية MailAsAttachment في MailMergeSettings على تعزيز حملات البريد الإلكتروني الخاصة بك عن طريق إرسال المستندات المدمجة كمرفقات لتحسين التفاعل.
type: docs
weight: 120
url: /ar/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

يُحدد أنه يجب إرسال المستندات الناتجة أثناء عملية دمج البريد كمرفقات بدلاً من كنص للبريد الإلكتروني نفسه. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool MailAsAttachment { get; set; }
```

## أمثلة

يوضح كيفية تنفيذ دمج البريد أثناء الاتصال بمصدر بيانات خارجي.

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

// يمكننا إعادة ضبط هذه الإعدادات بمسحها. بعد ذلك، نحفظ المستند،
// لن يقوم Microsoft Word بعد الآن بتنفيذ دمج البريد عندما نستخدمه لتحميل المستند.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### أنظر أيضا

* class [MailMergeSettings](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
