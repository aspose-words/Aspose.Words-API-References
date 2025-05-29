---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية AdvancedCompareOptions IgnoreStoreItemId على تحسين مقارنة المستندات من خلال تجاهل الاختلافات في معرف StructuredDocumentTag لتحسين الدقة.
type: docs
weight: 30
url: /ar/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

يحدد ما إذا كان سيتم تجاهل الاختلاف في معرف عنصر مخزن StructuredDocumentTag.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

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

* class [AdvancedCompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../../)
