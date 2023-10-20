---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words لـ .NET
description: DocumentBuilder Bold ملكية. صحيح إذا كان الخط منسقًا بالخط الغامق في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

صحيح إذا كان الخط منسقًا بالخط الغامق.

```csharp
public bool Bold { get; set; }
```

## أمثلة

يوضح كيفية تعبئة MERGEFIELDs بالبيانات باستخدام منشئ المستندات بدلاً من دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض حقول MERGEFIELDS، التي تقبل البيانات من الأعمدة التي تحمل نفس الاسم في مصدر بيانات أثناء دمج البريد،
// ثم املأها يدويًا.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
