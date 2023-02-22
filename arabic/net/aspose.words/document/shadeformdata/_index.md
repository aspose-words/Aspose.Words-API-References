---
title: Document.ShadeFormData
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج.
type: docs
weight: 360
url: /ar/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

يحدد ما إذا كان سيتم تشغيل التظليل الرمادي في حقول النموذج.

```csharp
public bool ShadeFormData { get; set; }
```

### أمثلة

يوضح كيفية تطبيق التظليل الرمادي على حقول النموذج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// يمكننا إيقاف التظليل الرمادي ، بحيث يندمج النص الذي تم وضع إشارة مرجعية عليه مع النص الآخر.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


