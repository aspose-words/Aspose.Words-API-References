---
title: DocumentBuilder.InsertStyleSeparator
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج فاصل النمط في المستند.
type: docs
weight: 460
url: /ar/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

إدراج فاصل النمط في المستند.

```csharp
public void InsertStyleSeparator()
```

### ملاحظات

تسمح هذه الطريقة بتطبيق أنماط فقرات مختلفة على جزأين مختلفين من سطر النص.

### أمثلة

يوضح كيفية العمل مع فواصل الأنماط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكن أن تحتوي كل فقرة على نمط واحد فقط.
// تتيح لنا طريقة InsertStyleSeparator التغلب على هذا القيد.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// يؤدي استدعاء الأسلوب InsertStyleSeparator إلى إنشاء فقرة أخرى،
// والتي يمكن أن يكون لها نمط مختلف عن السابق. لن يكون هناك فاصل بين الفقرات.
// سيبدو النص الموجود في مستند الإخراج كفقرة واحدة ذات نمطين.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


