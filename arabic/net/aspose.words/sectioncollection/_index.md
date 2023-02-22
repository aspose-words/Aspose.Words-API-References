---
title: Class SectionCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.SectionCollection فصل. مجموعة من الجزء كائنات في المستند .
type: docs
weight: 5450
url: /ar/net/aspose.words/sectioncollection/
---
## SectionCollection class

مجموعة من **الجزء** كائنات في المستند .

```csharp
public class SectionCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | استرداد قسم في الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | لتحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | إدراج عقدة في المجموعة بالفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | يزيل العقدة من المجموعة ومن الوثيقة. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | نسخ جميع الأقسام من المجموعة إلى مصفوفة جديدة من الأقسام. (2 methods) |

### ملاحظات

يمكن أن يحتوي مستند Microsoft Word على أقسام متعددة. لإنشاء قسم في Microsoft Word ، حدد الأمر Insert / Break وحدد نوع الفاصل. يحدد الفاصل ما إذا كان المقطع يبدأ على صفحة جديدة أو على نفس الصفحة.

يمكن استخدام إدراج الأقسام وإزالتها برمجيًا لتخصيص المستندات المنتجة_ أثناء دمج البريد. إذا كان المستند يحتاج إلى محتوى أو أجزاء مختلفة من محتوى بناءً على بعض المعايير ، فيمكنك إنشاء مستند "رئيسي" يحتوي على أقسام متعددة وحذف بعض الأقسام قبل دمج البريد أو بعده.

### أمثلة

يوضح كيفية إضافة وإزالة أقسام في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// احذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// قم بإلحاق نسخة مما هو الآن القسم الأول بنهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


