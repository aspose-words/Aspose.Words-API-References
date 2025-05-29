---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية ShadeFormData لتحسين رؤية النموذج باستخدام التظليل الرمادي، مما يحسن تجربة المستخدم وإمكانية الوصول.
type: docs
weight: 400
url: /ar/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

يحدد ما إذا كان سيتم تشغيل التظليل الرمادي على حقول النموذج.

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

// يمكننا إيقاف التظليل الرمادي، بحيث يمتزج النص الذي تم وضع إشارة مرجعية عليه مع النص الآخر.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
