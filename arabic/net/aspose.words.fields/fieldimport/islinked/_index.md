---
title: FieldImport.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: Aspose.Words لـ .NET
description: FieldImport IsLinked ملكية. الحصول على أو تعيين ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

الحصول على أو تعيين ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند.

```csharp
public bool IsLinked { get; set; }
```

## أمثلة

يوضح كيفية إدراج الصور باستخدام حقلي الاستيراد والتضمين.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يوجد أدناه نوعان متشابهان من الحقول يمكننا استخدامهما لعرض الصور المرتبطة من نظام الملفات المحلي.
// 1 - حقل التضمين:
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

* class [FieldImport](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
