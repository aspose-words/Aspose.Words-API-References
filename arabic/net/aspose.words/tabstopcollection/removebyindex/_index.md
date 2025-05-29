---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: Aspose.Words لـ .NET
description: أدر علامات التبويب بسهولة باستخدام طريقة RemoveByIndex. أزل أي علامة تبويب من مجموعتك بسرعة لتصميم مبسط.
type: docs
weight: 110
url: /ar/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

يزيل علامة التبويب عند الفهرس المحدد من المجموعة.

```csharp
public void RemoveByIndex(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | فهرس لمجموعة علامات التبويب. |

## أمثلة

يوضح كيفية تحديد علامة تبويب في مستند حسب فهرسها وإزالتها.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// قم بإزالة علامة التبويب الأولى.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
