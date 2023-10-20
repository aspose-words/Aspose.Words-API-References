---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words لـ .NET
description: Document IncludeTextboxesFootnotesEndnotesInStat ملكية. يحدد ما إذا كان سيتم تضمين مربعات النص والحواشي السفلية والتعليقات الختامية في إحصائيات عدد الكلمات في C#.
type: docs
weight: 220
url: /ar/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

يحدد ما إذا كان سيتم تضمين مربعات النص والحواشي السفلية والتعليقات الختامية في إحصائيات عدد الكلمات.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## أمثلة

يوضح كيفية تضمين أو استبعاد مربعات النص والحواشي السفلية والتعليقات الختامية من إحصائيات عدد الكلمات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// افتراضيًا، يتم تعيين الخيار على "خطأ".
doc.UpdateWordCount();
// يتم حساب الكلمات بدون مربعات النص والحواشي السفلية والتعليقات الختامية.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// يتم حساب الكلمات باستخدام مربعات النص والحواشي السفلية والتعليقات الختامية.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
