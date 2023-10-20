---
title: FieldIndex.PageNumberListSeparator
linktitle: PageNumberListSeparator
articleTitle: PageNumberListSeparator
second_title: Aspose.Words لـ .NET
description: FieldIndex PageNumberListSeparator ملكية. الحصول على أو تعيين تسلسل الأحرف المستخدم للفصل بين رقمي الصفحات في قائمة أرقام الصفحات في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.fields/fieldindex/pagenumberlistseparator/
---
## FieldIndex.PageNumberListSeparator property

الحصول على أو تعيين تسلسل الأحرف المستخدم للفصل بين رقمي الصفحات في قائمة أرقام الصفحات.

```csharp
public string PageNumberListSeparator { get; set; }
```

## أمثلة

يوضح كيفية تحرير فاصل رقم الصفحة في حقل INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء حقل INDEX الذي سيعرض إدخالاً لكل حقل XE موجود في المستند.
// سيعرض كل إدخال قيمة خاصية النص لحقل XE على الجانب الأيسر،
// ورقم الصفحة التي تحتوي على حقل XE على اليمين.
// سيقوم إدخال INDEX بتجميع حقول XE ذات القيم المطابقة في خاصية "النص".
// في إدخال واحد بدلاً من عمل إدخال لكل حقل XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// إذا كان حقل INDEX الخاص بنا يحتوي على إدخال لمجموعة من حقول XE،
// سيعرض هذا الإدخال رقم كل صفحة تحتوي على حقل XE ينتمي إلى هذه المجموعة.
// يمكننا تعيين فواصل مخصصة لتخصيص مظهر أرقام الصفحات هذه.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// بعد إدراج حقول XE هذه، سيعرض حقل INDEX "الإدخال الأول، في الصفحة (الصفحات) 2 و3 و4".
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### أنظر أيضا

* class [FieldIndex](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
