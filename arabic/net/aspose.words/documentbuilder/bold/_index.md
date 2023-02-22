---
title: DocumentBuilder.Bold
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder ملكية. True إذا كان تنسيق الخط عريض .
type: docs
weight: 20
url: /ar/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

True إذا كان تنسيق الخط عريض .

```csharp
public bool Bold { get; set; }
```

### أمثلة

يوضح كيفية تعبئة MERGEFIELD بالبيانات باستخدام أداة إنشاء المستندات بدلاً من دمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض MERGEFIELDS ، التي تقبل البيانات من أعمدة تحمل الاسم نفسه في مصدر بيانات أثناء دمج البريد ،
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


