---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.AdvancedCompareOptions لمقارنة مستندات فعّالة. خصّص الإعدادات للحصول على نتائج دقيقة وإنتاجية مُحسّنة.
type: docs
weight: 460
url: /ar/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

يسمح بتعيين خيارات المقارنة المتقدمة.

```csharp
public class AdvancedCompareOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | يحدد ما إذا كان سيتم تجاهل الاختلاف في معرف DrawingML الفريد. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | يحدد ما إذا كان سيتم تجاهل الاختلاف في معرف عنصر مخزن StructuredDocumentTag. |

## ملاحظات

لا يوجد لهذه الخيارات ما يعادلها في Microsoft Word وقد تساعد في إنتاج نتيجة مقارنة أكثر دقة.

## أمثلة

يوضح كيفية مقارنة SDT بنفس المحتوى ولكن بمعرفات عناصر متجر مختلفة.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// قم بتكوين الخيارات لمقارنة SDT بنفس المحتوى ولكن بمعرفات عناصر متجر مختلفة.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Comparing](../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../)
