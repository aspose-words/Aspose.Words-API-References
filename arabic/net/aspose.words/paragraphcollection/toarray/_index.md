---
title: ParagraphCollection.ToArray
second_title: Aspose.Words لمراجع .NET API
description: ParagraphCollection طريقة. نسخ كافة الفقرات من المجموعة إلى مجموعة جديدة من الفقرات.
type: docs
weight: 20
url: /ar/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

نسخ كافة الفقرات من المجموعة إلى مجموعة جديدة من الفقرات.

```csharp
public Paragraph[] ToArray()
```

### قيمة الإرجاع

مجموعة من الفقرات.

### أمثلة

يوضح كيفية إنشاء مصفوفة من NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

يوضح كيفية استخدام "الإزالة السريعة" لإزالة العقدة أثناء التعداد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// قم بإزالة عقدة من المجموعة الموجودة في منتصف التعداد.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* مساحة الاسم [Aspose.Words](../../paragraphcollection/)
* المجسم [Aspose.Words](../../../)


