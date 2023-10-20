---
title: OlePackage Class
linktitle: OlePackage
articleTitle: OlePackage
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.OlePackage فصل. يسمح بالوصول إلى خصائص حزمة OLE في C#.
type: docs
weight: 1160
url: /ar/net/aspose.words.drawing/olepackage/
---
## OlePackage class

يسمح بالوصول إلى خصائص حزمة OLE.

لمعرفة المزيد، قم بزيارة[العمل مع كائنات Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) مقالة توثيقية.

```csharp
public class OlePackage
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayName](../../aspose.words.drawing/olepackage/displayname/) { get; set; } | الحصول على اسم عرض حزمة OLE أو تعيينه. |
| [FileName](../../aspose.words.drawing/olepackage/filename/) { get; set; } | الحصول على اسم ملف حزمة OLE أو تعيينه. |

## ملاحظات

حزمة OLE هي طريقة قديمة و"غير موثقة" لتخزين الكائن المضمن إذا كان معالج OLE غير معروف. كانت إصدارات Windows المبكرة مثل Windows 3.1 و95 و98 تحتوي على تطبيق Packager.exe الذي يمكن استخدامه لتضمين أي نوع من البيانات في المستند . الآن تم استبعاد هذا التطبيق من Windows ولكن MS Word والتطبيقات الأخرى لا تزال تستخدمه لتضمين البيانات إذا كان معالج OLE مفقودًا أو غير معروف.

## أمثلة

يوضح كيفية إدراج كائن OLE في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا كائنات OLE بفتح ملفات أخرى في نظام الملفات المحلي باستخدام تطبيق آخر مثبت
// في نظام التشغيل الخاص بنا عن طريق النقر المزدوج على الشكل الذي يحتوي على كائن OLE في نص المستند.
// في هذه الحالة، سيكون ملفنا الخارجي عبارة عن أرشيف مضغوط بتنسيق ZIP.
byte[] zipFileBytes = File.ReadAllBytes(DatabaseDir + "cat001.zip");

using (MemoryStream stream = new MemoryStream(zipFileBytes))
{
    Shape shape = builder.InsertOleObject(stream, "Package", true, null);

    shape.OleFormat.OlePackage.FileName = "Package file name.zip";
    shape.OleFormat.OlePackage.DisplayName = "Package display name.zip";
}

doc.Save(ArtifactsDir + "Shape.InsertOlePackage.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
