---
title: CellFormat.SetPaddings
second_title: Aspose.Words لمراجع .NET API
description: CellFormat طريقة. يضبط مقدار المسافة بالنقاط المراد إضافتها إلى يسار/أعلى/يمين/أسفل محتويات الخلية.
type: docs
weight: 170
url: /ar/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

يضبط مقدار المسافة (بالنقاط) المراد إضافتها إلى يسار/أعلى/يمين/أسفل محتويات الخلية.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

### أمثلة

يوضح كيفية إضافة مسافة بيضاء إلى محتويات الخلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين مسافة الحشو (بالنقاط) بين الحدود ومحتويات النص
 // لكل خلية جدول نقوم بإنشائها باستخدام منشئ المستندات.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// أنشئ جدولًا يحتوي على خلية واحدة تحتوي محتوياتها على مسافة بيضاء.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### أنظر أيضا

* class [CellFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../cellformat/)
* المجسم [Aspose.Words](../../../)


