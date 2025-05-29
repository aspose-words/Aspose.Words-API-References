---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words لـ .NET
description: أدر تحديثات المستندات بسهولة باستخدام خاصية "FileInclude LockFields". تحكّم في تحرير الحقول وحسّن سلامة المستندات بسهولة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

يحصل على أو يحدد ما إذا كان سيتم منع تحديث الحقول في المستند المضمن.

```csharp
public bool LockFields { get; set; }
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
