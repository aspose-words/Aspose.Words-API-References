---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.FileCorruptedException، المصممة لمعالجة المستندات التالفة بسهولة أثناء التحميل. تمتع بإدارة سلسة للمستندات!
type: docs
weight: 3210
url: /ar/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

يتم طرحه أثناء تحميل المستند، عندما يبدو أن المستند تالف وغير قابل للتحميل.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class FileCorruptedException : Exception
```

## أمثلة

يوضح كيفية التقاط FileCorruptedException.

```csharp
try
{
    // إذا تلقينا رسالة خطأ "محتوى غير قابل للقراءة" عند محاولة فتح مستند باستخدام Microsoft Word،
    // هناك احتمالات بأن نحصل على استثناء عند محاولة تحميل هذا المستند باستخدام Aspose.Words.
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
