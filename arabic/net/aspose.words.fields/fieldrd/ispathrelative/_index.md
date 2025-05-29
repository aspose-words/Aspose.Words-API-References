---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsPathRelative في FieldRD لإدارة مسارات المستندات بسهولة. بسّط برمجة عملك بإعدادات مسارات مرنة لزيادة الكفاءة!
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

يحصل على أو يحدد ما إذا كان المسار نسبيًا للمستند الحالي.

```csharp
public bool IsPathRelative { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل RD لإنشاء إدخالات جدول المحتويات من العناوين الموجودة في مستندات أخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج جدول المحتويات،
// ثم قم بإضافة إدخال واحد لجدول المحتويات في الصفحة التالية.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// قم بإدراج حقل RD، والذي يشير إلى مستند نظام ملفات محلي آخر في خاصية FileName الخاصة به.
// سوف يقبل جدول المحتويات الآن أيضًا جميع العناوين من المستند المشار إليه كإدخالات لجدوله.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // قم بإنشاء المستند الذي يشير إليه حقل RD وأدرج عنوانًا.
// سيظهر هذا العنوان كمدخل في حقل جدول المحتويات في مستندنا الأول.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### أنظر أيضا

* class [FieldRD](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
