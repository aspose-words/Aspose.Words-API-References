---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words لـ .NET
description: TabStopCollection GetPositionByIndex طريقة. الحصول على موضع علامة التبويب بالنقاط عند الفهرس المحدد في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

الحصول على موضع علامة التبويب (بالنقاط) عند الفهرس المحدد.

```csharp
public double GetPositionByIndex(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس في مجموعة علامات الجدولة. |

### قيمة الإرجاع

موضع علامة التبويب.

## أمثلة

يوضح كيفية العثور على علامة تبويب والتوقف عند فهرسها والتحقق من موضعها.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// التحقق من موضع علامة التبويب الثانية في المجموعة.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
