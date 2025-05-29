---
title: FieldIncludePicture.ResizeHorizontally
linktitle: ResizeHorizontally
articleTitle: ResizeHorizontally
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تغيير حجم الصورة أفقيًا لتتمكن من تعديل أبعاد الصورة بسهولة لعرض مثالي. حسّن صورك بكل سهولة!
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldincludepicture/resizehorizontally/
---
## FieldIncludePicture.ResizeHorizontally property

يحصل على أو يحدد ما إذا كان سيتم تغيير حجم الصورة أفقيًا من المصدر.

```csharp
public bool ResizeHorizontally { get; set; }
```

## أمثلة

يوضح كيفية إدراج الصور باستخدام حقول IMPORT وINCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي نوعان متشابهان من الحقول يمكننا استخدامهما لعرض الصور المرتبطة من نظام الملفات المحلي.
// 1 - حقل INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// قم بتطبيق مرشح PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - حقل الاستيراد:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### أنظر أيضا

* class [FieldIncludePicture](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
