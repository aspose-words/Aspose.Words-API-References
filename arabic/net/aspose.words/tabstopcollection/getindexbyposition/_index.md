---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words لمراجع .NET API
description: TabStopCollection طريقة. الحصول على فهرس علامة الجدولة بالموضع المحدد بالنقاط.
type: docs
weight: 90
url: /ar/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

الحصول على فهرس علامة الجدولة بالموضع المحدد بالنقاط.

```csharp
public int GetIndexByPosition(double position)
```

### أمثلة

يوضح كيفية البحث عن موضع لمعرفة ما إذا كانت علامة الجدولة موجودة هناك والحصول على فهرسها.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// أضف علامة جدولة عند موضع 30 مم.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// نتيجة "0" التي يتم إرجاعها بواسطة "GetIndexByPosition" تؤكد توقف علامة التبويب
// عند 30 ملم موجود في هذه المجموعة، وهو عند الفهرس 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// يؤكد "-1" الذي تم إرجاعه بواسطة "GetIndexByPosition" ذلك
// لا توجد علامة جدولة في هذه المجموعة بموضع 60 مم.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../tabstopcollection/)
* المجسم [Aspose.Words](../../../)


