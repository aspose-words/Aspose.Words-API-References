---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words لمراجع .NET API
description: TabStopCollection طريقة. الحصول على فهرس علامة الجدولة مع الموضع المحدد بالنقاط .
type: docs
weight: 90
url: /ar/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

الحصول على فهرس علامة الجدولة مع الموضع المحدد بالنقاط .

```csharp
public int GetIndexByPosition(double position)
```

### أمثلة

يوضح كيفية البحث عن مركز لمعرفة ما إذا كانت هناك علامة جدولة موجودة والحصول على فهرسها.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// أضف علامة جدولة عند موضع 30 مم.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// نتيجة "0" التي تم إرجاعها بواسطة "GetIndexByPosition" تؤكد أن علامة الجدولة توقف
// في 30 مم موجود في هذه المجموعة ، وهو في الفهرس 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// A "-1" التي تم إرجاعها بواسطة "GetIndexByPosition" تؤكد ذلك
// لا توجد علامة جدولة في هذه المجموعة بموضع 60 مم.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../tabstopcollection/)
* المجسم [Aspose.Words](../../../)


