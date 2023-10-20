---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.TabStopCollection فصل. مجموعة منTabStop الكائنات التي تمثل علامات تبويب مخصصة لفقرة أو نمط في C#.
type: docs
weight: 6210
url: /ar/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

مجموعة من[`TabStop`](../tabstop/) الكائنات التي تمثل علامات تبويب مخصصة لفقرة أو نمط.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | الحصول على عدد علامات الجدولة في المجموعة. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | الحصول على علامة جدولة عند الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | إضافة علامة جدولة أو استبدالها في المجموعة. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | إضافة علامة جدولة أو استبدالها في المجموعة. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | الحصول على علامة الجدولة الأولى على يمين الموضع المحدد. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | الحصول على علامة الجدولة الأولى على يسار الموضع المحدد. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | حذف كافة مواضع علامات الجدولة. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | تحديد ما إذا كان الكائن المحدد يساوي قيمة الكائن الحالي. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | تحديد ما إذا كان المحدد`TabStopCollection` يساوي القيمة الحالية`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | بمثابة دالة تجزئة لهذا النوع. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | الحصول على فهرس علامة الجدولة بالموضع المحدد بالنقاط. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | الحصول على موضع علامة التبويب (بالنقاط) عند الفهرس المحدد. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | إزالة علامة الجدولة عند الفهرس المحدد من المجموعة. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | إزالة علامة الجدولة عند الموضع المحدد من المجموعة. |

## ملاحظات

في مستندات Microsoft Word، يمكن تعريف علامة الجدولة في خصائص نمط الفقرة أو مباشرة في خصائص الفقرة. يمكن أن يعتمد النمط على نمط آخر. وبالتالي، فإن المجموعة الكاملة من علامات الجدولة لكائن معين هي عبارة عن مجموعة من علامات الجدولة المحددة مباشرة على هذا الكائن وعلامات الجدولة الموروثة من الأنماط الأصلية.

في Aspose.Words، عندما تحصل على ملف`TabStopCollection`بالنسبة لفقرة أو نمط، فهو يحتوي فقط على علامات الجدولة المخصصة المحددة مباشرة لهذه الفقرة أو النمط. لا تتضمن المجموعة علامات الجدولة المحددة في الأنماط الأصلية أو علامات الجدولة الافتراضية.

## أمثلة

يوضح كيفية التعامل مع مجموعة علامات الجدولة الخاصة بالمستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 نقطة هي "بوصة" واحدة في مسطرة إيقاف علامة التبويب في Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// يأخذ كل حرف "علامة تبويب" مؤشر المنشئ إلى موقع علامة التبويب التالية.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// تحصل كل فقرة على مجموعة علامات الجدولة الخاصة بها، والتي تستنسخ قيمها من مجموعة علامات الجدولة الخاصة بمنشئ المستندات.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// يمكن أن توجهنا مجموعة علامات التبويب إلى TabStops قبل وبعد مواضع معينة.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// يمكننا مسح مجموعة علامات الجدولة الخاصة بالفقرة للعودة إلى سلوك الجدولة الافتراضي.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### أنظر أيضا

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
