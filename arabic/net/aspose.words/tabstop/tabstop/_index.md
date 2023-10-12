---
title: TabStop.TabStop
second_title: Aspose.Words لمراجع .NET API
description: TabStop البناء. تهيئة مثيل جديد لهذه الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words/tabstop/tabstop/
---
## TabStop(double) {#constructor}

تهيئة مثيل جديد لهذه الفئة.

```csharp
public TabStop(double position)
```

### أمثلة

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

* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../tabstop/)
* المجسم [Aspose.Words](../../../)

---

## TabStop(double, TabAlignment, TabLeader) {#constructor_1}

تهيئة مثيل جديد لهذه الفئة.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | موضع علامة التبويب بالنقاط. |
| alignment | TabAlignment | أ[`TabAlignment`](../../tabalignment/) تحدد القيمة that محاذاة النص عند علامة التبويب هذه. |
| leader | TabLeader | أ[`TabLeader`](../../tableader/) القيمة التي تحدد نوع السطر الرئيسي المعروض أسفل حرف علامة التبويب. |

### أمثلة

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

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../tabstop/)
* المجسم [Aspose.Words](../../../)


