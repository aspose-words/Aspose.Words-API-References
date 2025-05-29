---
title: SectionCollection Class
linktitle: SectionCollection
articleTitle: SectionCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.SectionCollection—الحل الأمثل لإدارة أقسام المستندات بكفاءة مع ميزات قوية ومرونة.
type: docs
weight: 6570
url: /ar/net/aspose.words/sectioncollection/
---
## SectionCollection class

مجموعة من[`Section`](../section/) الكائنات الموجودة في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الأقسام](https://docs.aspose.com/words/net/working-with-sections/) مقالة توثيقية.

```csharp
public class SectionCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | يسترجع قسمًا في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | يعيد الفهرس المبني على الصفر للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | نسخ جميع الأقسام من المجموعة إلى مجموعة جديدة من الأقسام. (2 methods) |

## ملاحظات

يمكن أن يحتوي مستند مايكروسوفت وورد على عدة أقسام. لإنشاء قسم في مايكروسوفت وورد، حدد أمر "إدراج/فصل" وحدد نوع الفصل. يحدد الفصل ما إذا كان القسم سيبدأ في صفحة جديدة أم في الصفحة نفسها.

يمكن استخدام إدراج الأقسام وإزالتها برمجيًا لتخصيص المستندات المُنتَجة أثناء دمج البريد. إذا احتاج مستند إلى محتوى مختلف أو أجزاء مختلفة من محتوى x000d_ بناءً على بعض المعايير، فيمكنك إنشاء مستند "رئيسي" يحتوي على أقسام متعددة وحذف بعض الأقسام قبل دمج البريد أو بعده.

## أمثلة

يوضح كيفية إضافة أقسام وإزالتها في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

//حذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// قم بإضافة نسخة من القسم الأول إلى نهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
