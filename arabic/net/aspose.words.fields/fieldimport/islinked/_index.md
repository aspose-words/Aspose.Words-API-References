---
title: FieldImport.IsLinked
second_title: Aspose.Words لمراجع .NET API
description: FieldImport ملكية. الحصول على أو تحديد ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

الحصول على أو تحديد ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند.

```csharp
public bool IsLinked { get; set; }
```

### أمثلة

يوضح كيفية إدراج الصور باستخدام حقلي IMPORT و INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يوجد أدناه نوعان متشابهان من الحقول يمكننا استخدامهما لعرض الصور المرتبطة من نظام الملفات المحلي.
// 1 - حقل INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// تطبيق مرشح PNG32.FLT.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldimport/)
* المجسم [Aspose.Words](../../../)


