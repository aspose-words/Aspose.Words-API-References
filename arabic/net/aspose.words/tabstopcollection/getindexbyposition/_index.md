---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة TabStopCollection GetIndexByPosition للعثور بسهولة على فهرس علامة التبويب عند أي موضع محدد. مثالية للتحكم الدقيق في التخطيط!
type: docs
weight: 90
url: /ar/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

يحصل على فهرس علامة التبويب مع الموضع المحدد بالنقاط.

```csharp
public int GetIndexByPosition(double position)
```

## أمثلة

يوضح كيفية البحث عن موضع لمعرفة ما إذا كانت علامة التبويب موجودة هناك والحصول على فهرسها.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

//أضف علامة تبويب عند موضع 30 مم.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// تؤكد النتيجة "0" التي تم إرجاعها بواسطة "GetIndexByPosition" أن علامة التبويب موجودة
// يوجد 30 مم في هذه المجموعة، وهو موجود عند الفهرس 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// يؤكد "-1" الذي تم إرجاعه بواسطة "GetIndexByPosition" أن
// لا يوجد علامة تبويب في هذه المجموعة بموضع 60 مم.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
