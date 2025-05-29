---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك باستخدام طريقة InsertStyleSeparator في DocumentBuilder، وقم بإضافة فواصل الأنماط بسهولة لتحسين التنسيق والتنظيم.
type: docs
weight: 490
url: /ar/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

إدراج فاصل النمط في المستند.

```csharp
public void InsertStyleSeparator()
```

## ملاحظات

تسمح هذه الطريقة بتطبيق أنماط فقرة مختلفة على جزأين مختلفين من سطر النص.

## أمثلة

يوضح كيفية العمل مع فواصل الأنماط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة لا يمكن أن يكون لها سوى نمط واحد.
// تسمح لنا طريقة InsertStyleSeparator بالتغلب على هذا القيد.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// يؤدي استدعاء طريقة InsertStyleSeparator إلى إنشاء فقرة أخرى،
// يمكن أن يكون له نمط مختلف عن السابق. لن يكون هناك فاصل بين الفقرات.
//سيبدو النص في المستند الناتج وكأنه فقرة واحدة ذات نمطين.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
