---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words لـ .NET
description: ViewOptions FormsDesign ملكية. يحدد ما إذا كانت الوثيقة في وضع تصميم النماذج في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

يحدد ما إذا كانت الوثيقة في وضع تصميم النماذج.

```csharp
public bool FormsDesign { get; set; }
```

## ملاحظات

يعمل حاليًا فقط مع المستندات بتنسيق WordML.

## أمثلة

يوضح كيفية تمكين/تعطيل وضع تصميم النماذج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بتعيين خاصية "FormsDesign" على "خطأ" لإبقاء وضع تصميم النماذج معطلاً.
// اضبط خاصية "FormsDesign" على "true" لتمكين وضع تصميم النماذج.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
