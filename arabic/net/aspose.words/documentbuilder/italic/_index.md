---
title: DocumentBuilder.Italic
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder ملكية. صحيح إذا كان الخط منسقًا بالخط المائل.
type: docs
weight: 140
url: /ar/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

صحيح إذا كان الخط منسقًا بالخط المائل.

```csharp
public bool Italic { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


