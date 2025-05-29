---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words لـ .NET
description: تأكد من توافق مستندات OOXML الخاصة بك مع معايير الامتثال بسهولة. تُحلل أداتنا المحتوى للتحقق من توافق OOXML، مما يُعزز سلامة المستندات.
type: docs
weight: 70
url: /ar/net/aspose.words/document/compliance/
---
## Document.Compliance property

يحصل على إصدار التوافق مع OOXML المحدد من محتوى المستند المحمّل. يكون منطقيًا فقط بالنسبة لمستندات OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## ملاحظات

إذا قمت بإنشاء مستند فارغ جديد أو تحميل مستند غير OOXML، فإن document يعيدEcma376_2006 قيمة.

## أمثلة

يوضح كيفية قراءة إصدار التوافق مع Open Office XML للمستند المحمّل.

```csharp
// يختلف إصدار التوافق بين المستندات التي تم إنشاؤها بواسطة إصدارات مختلفة من Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### أنظر أيضا

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
