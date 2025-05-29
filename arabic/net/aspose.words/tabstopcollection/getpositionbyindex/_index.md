---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة TabStopCollection GetPositionByIndex للعثور بسهولة على مواضع علامات التبويب في نقاط حسب الفهرس. حسّن تصميمك بسهولة!
type: docs
weight: 100
url: /ar/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

يحصل على موضع (بالنقاط) علامة التبويب عند الفهرس المحدد.

```csharp
public double GetPositionByIndex(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس لمجموعة علامات التبويب. |

### قيمة الإرجاع

موضع علامة التبويب.

## أمثلة

يوضح كيفية العثور على علامة تبويب والتوقف عند فهرسها والتحقق من موقعها.

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
