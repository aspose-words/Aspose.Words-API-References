---
title: FieldIncludePicture.ResizeHorizontally
linktitle: ResizeHorizontally
articleTitle: ResizeHorizontally
second_title: Aspose.Words لـ .NET
description: FieldIncludePicture ResizeHorizontally ملكية. الحصول على أو تعيين ما إذا كان سيتم تغيير حجم الصورة أفقيًا من المصدر في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldincludepicture/resizehorizontally/
---
## FieldIncludePicture.ResizeHorizontally property

الحصول على أو تعيين ما إذا كان سيتم تغيير حجم الصورة أفقيًا من المصدر.

```csharp
public bool ResizeHorizontally { get; set; }
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

* class [FieldIncludePicture](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
