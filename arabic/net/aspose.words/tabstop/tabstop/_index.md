---
title: TabStop
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ TabStop، وأنشئ وخصّص المثيلات بسهولة لتحسين وظائف مشاريعك. حسّن كفاءة البرمجة لديك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words/tabstop/tabstop/
---
## TabStop(*double*) {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public TabStop(double position)
```

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

* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## TabStop(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public TabStop(double position, TabAlignment alignment, TabLeader leader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | موضع علامة التبويب بالنقاط. |
| alignment | TabAlignment | أ[`TabAlignment`](../../tabalignment/) القيمة that تحدد محاذاة النص عند علامة التبويب هذه. |
| leader | TabLeader | أ[`TabLeader`](../../tableader/) القيمة التي تحدد نوع الخط الرئيسي المعروض أسفل حرف التبويب. |

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

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
