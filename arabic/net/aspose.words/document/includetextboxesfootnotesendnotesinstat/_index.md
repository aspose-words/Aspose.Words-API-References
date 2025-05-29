---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words لـ .NET
description: حسّن عدد كلمات مستندك باستخدام خاصية "IncludeTextboxesFootnotesEndnotesInStat". تحكم في مربعات النص والحواشي السفلية والختامية بسهولة!
type: docs
weight: 230
url: /ar/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

يحدد ما إذا كان سيتم تضمين مربعات النص والحواشي السفلية والختامية في إحصائيات عدد الكلمات.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## أمثلة

يوضح كيفية تضمين أو استبعاد مربعات النص والحواشي السفلية والختامية من إحصائيات عدد الكلمات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// بشكل افتراضي يتم تعيين الخيار على 'false'.
doc.UpdateWordCount();
// يتم احتساب الكلمات دون الحاجة إلى مربعات نصية وحواشي سفلية ونهاية.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// يتم حساب الكلمات باستخدام مربعات النص والحواشي السفلية والحواشي النهائية.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
