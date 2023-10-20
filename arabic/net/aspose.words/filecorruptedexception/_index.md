---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words لـ .NET
description: Aspose.Words.FileCorruptedException فصل. يتم طرحه أثناء تحميل المستند عندما يبدو المستند تالفًا ومن المستحيل تحميله في C#.
type: docs
weight: 2800
url: /ar/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

يتم طرحه أثناء تحميل المستند، عندما يبدو المستند تالفًا ومن المستحيل تحميله.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class FileCorruptedException : Exception
```

## أمثلة

يوضح كيفية التقاط FileCorruptedException.

```csharp
try
{
    // إذا تلقينا رسالة خطأ "محتوى غير قابل للقراءة" عند محاولة فتح مستند باستخدام Microsoft Word،
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
