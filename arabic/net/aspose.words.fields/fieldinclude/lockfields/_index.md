---
title: FieldInclude.LockFields
second_title: Aspose.Words لمراجع .NET API
description: FieldInclude ملكية. الحصول على أو تعيين ما إذا كان سيتم منع تحديث الحقول الموجودة في المستند المضمن.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

الحصول على أو تعيين ما إذا كان سيتم منع تحديث الحقول الموجودة في المستند المضمن.

```csharp
public bool LockFields { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Fields](../../fieldinclude/)
* المجسم [Aspose.Words](../../../)


