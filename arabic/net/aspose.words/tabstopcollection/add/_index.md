---
title: TabStopCollection.Add
second_title: Aspose.Words لمراجع .NET API
description: TabStopCollection طريقة. إضافة علامة جدولة أو استبدالها في المجموعة.
type: docs
weight: 30
url: /ar/net/aspose.words/tabstopcollection/add/
---
## Add(TabStop) {#add}

إضافة علامة جدولة أو استبدالها في المجموعة.

```csharp
public void Add(TabStop tabStop)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tabStop | TabStop | كائن علامة جدولة لإضافته. |

### ملاحظات

إذا كانت علامة الجدولة موجودة بالفعل في الموضع المحدد، فسيتم استبدالها.

### أمثلة

يوضح كيفية إضافة علامات جدولة مخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// فيما يلي طريقتان لإضافة علامات الجدولة إلى مجموعة علامات الجدولة الخاصة بالفقرة عبر خاصية "ParagraphFormat".
// 1 - قم بإنشاء كائن "TabStop"، ثم قم بإضافته إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة التبويب الجديدة إلى طريقة "الإضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// أضف علامات الجدولة عند 5 سم لجميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// يأخذ كل حرف "علامة تبويب" مؤشر المنشئ إلى موقع علامة التبويب التالية.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### أنظر أيضا

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../tabstopcollection/)
* المجسم [Aspose.Words](../../../)

---

## Add(double, TabAlignment, TabLeader) {#add_1}

إضافة علامة جدولة أو استبدالها في المجموعة.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | الموضع (بالنقاط) الذي تريد إضافة علامة الجدولة إليه. |
| alignment | TabAlignment | أ[`TabAlignment`](../../tabalignment/) تحدد القيمة that محاذاة النص عند علامة الجدولة. |
| leader | TabLeader | أ[`TabLeader`](../../tableader/) تحدد القيمة that نوع السطر الرئيسي المعروض أسفل حرف علامة التبويب. |

### ملاحظات

إذا كانت علامة الجدولة موجودة بالفعل في الموضع المحدد، فسيتم استبدالها.

### أمثلة

يوضح كيفية إضافة علامات جدولة مخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// فيما يلي طريقتان لإضافة علامات الجدولة إلى مجموعة علامات الجدولة الخاصة بالفقرة عبر خاصية "ParagraphFormat".
// 1 - قم بإنشاء كائن "TabStop"، ثم قم بإضافته إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة التبويب الجديدة إلى طريقة "الإضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// أضف علامات الجدولة عند 5 سم لجميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// يأخذ كل حرف "علامة تبويب" مؤشر المنشئ إلى موقع علامة التبويب التالية.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### أنظر أيضا

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../tabstopcollection/)
* المجسم [Aspose.Words](../../../)


