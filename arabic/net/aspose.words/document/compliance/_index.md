---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words لـ .NET
description: Document Compliance ملكية. الحصول على إصدار توافق OOXML المحدد من محتوى المستند الذي تم تحميله. هذا منطقي فقط لمستندات OOXML في C#.
type: docs
weight: 60
url: /ar/net/aspose.words/document/compliance/
---
## Document.Compliance property

الحصول على إصدار توافق OOXML المحدد من محتوى المستند الذي تم تحميله. هذا منطقي فقط لمستندات OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## ملاحظات

إذا قمت بإنشاء مستند فارغ جديد أو قمت بتحميل مستند غير OOXML، فسيتم إرجاع ملف document Ecma376_2006 قيمة.

## أمثلة

يوضح كيفية قراءة إصدار توافق Open Office XML الخاص بالمستند الذي تم تحميله.

```csharp
// يختلف إصدار الامتثال بين المستندات التي تم إنشاؤها بواسطة إصدارات مختلفة من Microsoft Word.
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
