---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.TabStopCollection. أدر بسهولة علامات تبويب مخصصة للفقرات والأنماط، مما يُحسّن تنسيق مستنداتك بدقة.
type: docs
weight: 7060
url: /ar/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

مجموعة من[`TabStop`](../tabstop/) الكائنات التي تمثل علامات تبويب مخصصة لفقرة أو نمط.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | يحصل على عدد علامات التبويب في المجموعة. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | يحصل على علامة تبويب عند الفهرس المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | يضيف أو يستبدل علامة تبويب في المجموعة. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | يضيف أو يستبدل علامة تبويب في المجموعة. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | يحصل على علامة تبويب أولى على يمين الموضع المحدد. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | يحصل على علامة تبويب أولى على يسار الموضع المحدد. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | يحذف جميع مواضع علامة التبويب. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | يحدد ما إذا كان الكائن المحدد يساوي في القيمة الكائن الحالي. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | يحدد ما إذا كان المحدد`TabStopCollection` يساوي القيمة الحالية`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | يعمل كدالة تجزئة لهذا النوع. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | يحصل على فهرس علامة التبويب مع الموضع المحدد بالنقاط. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | يحصل على موضع (بالنقاط) علامة التبويب عند الفهرس المحدد. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | يزيل علامة التبويب عند الفهرس المحدد من المجموعة. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | يزيل علامة التبويب في الموضع المحدد من المجموعة. |

## ملاحظات

في مستندات مايكروسوفت وورد، يمكن تعريف علامة الجدولة ضمن خصائص نمط paragraph أو مباشرةً ضمن خصائص الفقرة. يمكن أن يستند النمط إلى نمط آخر. . لذلك، فإن المجموعة الكاملة لعلامات الجدولة لكائن معين هي مزيج من علامات الجدولة المُعرّفة مباشرةً في هذا الكائن وعلامات الجدولة الموروثة من الأنماط الأصلية.

في Aspose.Words، عندما تحصل على`TabStopCollection` بالنسبة لفقرة أو نمط، فهي تحتوي فقط على علامات التبويب المخصصة المحددة مباشرة لهذه الفقرة أو النمط. لا تتضمن المجموعة علامات التبويب المحددة في الأنماط الأصلية أو علامات التبويب الافتراضية.

## أمثلة

يوضح كيفية العمل مع مجموعة علامات التبويب الموجودة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 نقطة هي "بوصة" واحدة على مسطرة علامة التبويب في برنامج Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// كل حرف "علامة تبويب" يأخذ مؤشر المنشئ إلى موقع علامة التبويب التالية.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// تحصل كل فقرة على مجموعة علامات التبويب الخاصة بها، والتي تستنسخ قيمها من مجموعة علامات التبويب الخاصة بمنشئ المستندات.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// يمكن لمجموعة علامات التبويب أن تشير إلينا إلى علامات التبويب قبل وبعد مواضع معينة.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// يمكننا مسح مجموعة علامات التبويب الخاصة بالفقرة للعودة إلى سلوك علامات التبويب الافتراضي.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### أنظر أيضا

* class [InternableComplexAttr](../internablecomplexattr/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
