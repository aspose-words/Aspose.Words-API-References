---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CellFormat SetPaddings لتخصيص المسافة بين الخلايا في نقاط، مما يعزز تخطيطك لتحسين القراءة والتصميم.
type: docs
weight: 170
url: /ar/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

يحدد مقدار المساحة (بالنقاط) التي يجب إضافتها إلى اليسار/الأعلى/اليمين/الأسفل من محتويات الخلية.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## أمثلة

يوضح كيفية ملء محتويات الخلية بالمسافات البيضاء.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين مسافة الحشو (بالنقاط) بين الحدود ومحتويات النص
 // لكل خلية جدول نقوم بإنشائها باستخدام منشئ المستندات.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// قم بإنشاء جدول يحتوي على خلية واحدة تحتوي محتوياتها على مسافة بيضاء.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### أنظر أيضا

* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
