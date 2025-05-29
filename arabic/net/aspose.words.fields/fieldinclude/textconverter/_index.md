---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldInclude TextConverter—يمكنك بسهولة إدارة تحويلات تنسيقات الملفات باستخدام أسماء محولات النصوص القابلة للتخصيص لتحسين كفاءة سير العمل.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

يحصل على اسم محول النص لتنسيق الملف المضمن أو يعينه.

```csharp
public string TextConverter { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حقل INCLUDE وتعيين خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام حقل INCLUDE لاستيراد جزء من مستند آخر في نظام الملفات المحلي.
// تحتوي الإشارة المرجعية من المستند الآخر الذي نشير إليه بهذا الحقل على هذا الجزء المستورد.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### أنظر أيضا

* class [FieldInclude](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
