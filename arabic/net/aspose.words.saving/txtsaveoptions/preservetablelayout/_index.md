---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة PreserveTableLayout في TxtSaveOptions، التي تضمن احتفاظ جداولك بتنسيقها عند حفظها كنص عادي. حسّن قابلية قراءة مستندك!
type: docs
weight: 50
url: /ar/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

يحدد ما إذا كان ينبغي للبرنامج محاولة الحفاظ على تخطيط الجداول عند الحفظ بتنسيق نص عادي. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## أمثلة

يوضح كيفية الحفاظ على تخطيط الجداول عند التحويل إلى نص عادي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// اضبط خاصية "PreserveTableLayout" على "true" لتطبيق حشو المسافات البيضاء على المحتويات
// من مستند النص العادي الناتج للحفاظ على أكبر قدر ممكن من تخطيط الجدول.
// اضبط خاصية "PreserveTableLayout" على "false" لحفظ محتويات جميع الجداول
// كجسم نصي مستمر، مع سطر جديد فقط لكل صف.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### أنظر أيضا

* class [TxtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
