---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة TabStopCollection Add بإضافة علامات التبويب أو تحديثها بكفاءة، مما يعمل على تحسين تخطيط مستندك وتنسيقه.
type: docs
weight: 30
url: /ar/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

يضيف أو يستبدل علامة تبويب في المجموعة.

```csharp
public void Add(TabStop tabStop)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tabStop | TabStop | كائن علامة التبويب لإضافته. |

## ملاحظات

إذا كانت علامة التبويب موجودة بالفعل في الموضع المحدد، فسيتم استبدالها.

## أمثلة

يوضح كيفية إضافة علامات تبويب مخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// فيما يلي طريقتان لإضافة علامات التبويب إلى مجموعة علامات التبويب الخاصة بالفقرة عبر خاصية "ParagraphFormat".
// 1 - قم بإنشاء كائن "TabStop"، ثم أضفه إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة التبويب الجديدة إلى طريقة "إضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// أضف علامات التبويب على مسافة 5 سم إلى جميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// كل حرف "علامة تبويب" يأخذ مؤشر المنشئ إلى موقع علامة التبويب التالية.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### أنظر أيضا

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

يضيف أو يستبدل علامة تبويب في المجموعة.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | موضع (بالنقاط) حيث سيتم إضافة علامة التبويب. |
| alignment | TabAlignment | أ[`TabAlignment`](../../tabalignment/) القيمة that تحدد محاذاة النص عند علامة التبويب. |
| leader | TabLeader | أ[`TabLeader`](../../tableader/)القيمة that تحدد نوع الخط الرئيسي المعروض أسفل حرف التبويب. |

## ملاحظات

إذا كانت علامة التبويب موجودة بالفعل في الموضع المحدد، فسيتم استبدالها.

## أمثلة

يوضح كيفية إضافة علامات تبويب مخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// فيما يلي طريقتان لإضافة علامات التبويب إلى مجموعة علامات التبويب الخاصة بالفقرة عبر خاصية "ParagraphFormat".
// 1 - قم بإنشاء كائن "TabStop"، ثم أضفه إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة التبويب الجديدة إلى طريقة "إضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// أضف علامات التبويب على مسافة 5 سم إلى جميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// كل حرف "علامة تبويب" يأخذ مؤشر المنشئ إلى موقع علامة التبويب التالية.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### أنظر أيضا

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
