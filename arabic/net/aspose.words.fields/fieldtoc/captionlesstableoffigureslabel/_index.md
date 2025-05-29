---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldToc CaptionlessTableOfFiguresLabel لتخصيص جدول الأشكال. أدر مُعرّفات التسلسل بسهولة دون الحاجة إلى تسميات توضيحية!
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

يحصل على اسم معرف التسلسل المستخدم عند إنشاء جدول الأشكال الذي لا يتضمن تسمية ورقم التسمية التوضيحية أو يعينه.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## أمثلة

يوضح كيفية تعيين اسم معرف التسلسل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### أنظر أيضا

* class [FieldToc](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
