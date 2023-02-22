---
title: Class FileCorruptedException
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.FileCorruptedException فصل. تم إلقاؤه أثناء تحميل المستند  عندما يبدو أن المستند تالف ويستحيل تحميله.
type: docs
weight: 2620
url: /ar/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

تم إلقاؤه أثناء تحميل المستند ، عندما يبدو أن المستند تالف ويستحيل تحميله.

```csharp
public class FileCorruptedException : Exception
```

### أمثلة

يوضح كيفية التقاط ملف FileCorruptException.

```csharp
try
{
    // إذا تلقينا رسالة خطأ "محتوى غير قابل للقراءة" عند محاولة فتح مستند باستخدام Microsoft Word ،
    // من المحتمل أننا سنحصل على استثناء عند محاولة تحميل هذا المستند باستخدام Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


