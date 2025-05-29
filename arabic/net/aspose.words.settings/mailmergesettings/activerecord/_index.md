---
title: MailMergeSettings.ActiveRecord
linktitle: ActiveRecord
articleTitle: ActiveRecord
second_title: Aspose.Words لـ .NET
description: اكتشف إعدادات دمج البريد. خصّص مستندات مايكروسوفت وورد باختيار فهرس السجلات المطلوب من مصدر بياناتك. ابدأ بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.settings/mailmergesettings/activerecord/
---
## MailMergeSettings.ActiveRecord property

يُحدد فهرس السجل من مصدر البيانات الذي سيتم عرضه في Microsoft Word. القيمة الافتراضية هي 1.

```csharp
public int ActiveRecord { get; set; }
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
