---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words لـ .NET
description: Document ShadeFormData ملكية. يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج في C#.
type: docs
weight: 380
url: /ar/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج.

```csharp
public bool ShadeFormData { get; set; }
```

## أمثلة

يوضح كيفية تطبيق التظليل الرمادي على حقول النموذج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// يمكننا إيقاف التظليل الرمادي، بحيث يمتزج النص ذو الإشارة المرجعية مع النص الآخر.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
