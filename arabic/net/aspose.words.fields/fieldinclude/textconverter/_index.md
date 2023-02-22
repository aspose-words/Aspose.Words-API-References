---
title: FieldInclude.TextConverter
second_title: Aspose.Words لمراجع .NET API
description: FieldInclude ملكية. الحصول على أو تحديد اسم محول النص لتنسيق الملف المضمن.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

الحصول على أو تحديد اسم محول النص لتنسيق الملف المضمن.

```csharp
public string TextConverter { get; set; }
```

### أمثلة

يوضح كيفية إنشاء حقل INCLUDE وتعيين خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام حقل INCLUDE لاستيراد جزء من مستند آخر في نظام الملفات المحلي.
// تحتوي الإشارة المرجعية من المستند الآخر التي نشير إليها مع هذا الحقل على هذا الجزء المستورد.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldinclude/)
* المجسم [Aspose.Words](../../../)


