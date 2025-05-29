---
title: TabStopCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى علامات التبويب بسهولة باستخدام خاصية TabStopCollection Item. استرجع علامات تبويب محددة حسب الفهرس لتصفح فعال لواجهة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

يحصل على علامة تبويب عند الفهرس المحدد.

```csharp
public TabStop this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس لمجموعة علامات التبويب. |

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

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## TabStopCollection indexer (2 of 2)

يحصل على علامة تبويب عند الموضع المحدد.

```csharp
public TabStop this[double position] { get; }
```

| معامل | وصف |
| --- | --- |
| position | موضع (بالنقاط) علامة التبويب. |

## ملاحظات

إرجاع`باطل` إذا لم يتم العثور على علامة تبويب في الموضع المحدد.

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

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
