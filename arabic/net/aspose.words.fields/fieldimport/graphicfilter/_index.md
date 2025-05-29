---
title: FieldImport.GraphicFilter
linktitle: GraphicFilter
articleTitle: GraphicFilter
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldImport GraphicFilter لتعيين أو استرداد مرشحات تنسيق الرسوميات بسهولة، مما يعزز عملية إدراج المحتوى لديك.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldimport/graphicfilter/
---
## FieldImport.GraphicFilter property

يحصل على اسم المرشح أو يعينه لتنسيق الرسم البياني الذي سيتم إدراجه.

```csharp
public string GraphicFilter { get; set; }
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

* class [FieldImport](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
