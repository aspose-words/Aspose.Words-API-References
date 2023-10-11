---
title: FieldRD.FileName
second_title: Aspose.Words لمراجع .NET API
description: FieldRD ملكية. الحصول على أو تعيين اسم الملف الذي سيتم تضمينه عند إنشاء جدول محتويات أو جدول المراجع أو الفهرس.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

الحصول على أو تعيين اسم الملف الذي سيتم تضمينه عند إنشاء جدول محتويات، أو جدول المراجع، أو الفهرس.

```csharp
public string FileName { get; set; }
```

### أمثلة

يظهر كيفية استخدام حقل RD لإنشاء جدول محتويات الإدخالات من العناوين في المستندات الأخرى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج جدول المحتويات،
// ثم قم بإضافة إدخال واحد لجدول المحتويات في الصفحة التالية.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// أدخل حقل RD، الذي يشير إلى مستند نظام ملفات محلي آخر في خاصية FileName الخاصة به.
// سيقبل جدول المحتويات الآن أيضًا جميع العناوين من المستند المشار إليه كمدخلات لجدوله.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // أنشئ المستند الذي يشير إليه حقل RD وأدخل عنوانًا.
// سيظهر هذا العنوان كإدخال في حقل جدول المحتويات (TOC) في وثيقتنا الأولى.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldrd/)
* المجسم [Aspose.Words](../../../)


