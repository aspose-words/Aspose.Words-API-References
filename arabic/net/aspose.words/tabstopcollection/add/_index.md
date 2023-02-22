---
title: TabStopCollection.Add
second_title: Aspose.Words لمراجع .NET API
description: TabStopCollection طريقة. إضافة أو استبدال علامة الجدولة في المجموعة.
type: docs
weight: 30
url: /ar/net/aspose.words/tabstopcollection/add/
---
## Add(TabStop) {#add}

إضافة أو استبدال علامة الجدولة في المجموعة.

```csharp
public void Add(TabStop tabStop)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| tabStop | TabStop | كائن توقف جدولة لإضافته. |

### ملاحظات

إذا كانت علامة الجدولة موجودة بالفعل في الموضع المحدد ، فسيتم استبدالها.

### أمثلة

يوضح كيفية إضافة علامات الجدولة المخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// يوجد أدناه طريقتان لإضافة علامات الجدولة إلى مجموعة فقرة من علامات الجدولة عبر خاصية "تنسيق الفقرة".
// 1 - أنشئ كائن "TabStop" ، ثم أضفه إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة تبويب جديدة إلى طريقة "إضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// إضافة علامات الجدولة عند 5 سم لجميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// كل حرف "علامة تبويب" يأخذ مؤشر المنشئ إلى موقع علامة الجدولة التالية.
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

إضافة أو استبدال علامة الجدولة في المجموعة.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | موضع (بالنقاط) حيث يتم إضافة علامة الجدولة. |
| alignment | TabAlignment | أ[`TabAlignment`](../../tabalignment/)تحدد القيمة that محاذاة النص عند علامة الجدولة. |
| leader | TabLeader | أ[`TabLeader`](../../tableader/) تحدد القيمة that نوع السطر الرئيسي المعروض أسفل حرف الجدولة. |

### ملاحظات

إذا كانت علامة الجدولة موجودة بالفعل في الموضع المحدد ، فسيتم استبدالها.

### أمثلة

يوضح كيفية إضافة علامات الجدولة المخصصة إلى مستند.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// يوجد أدناه طريقتان لإضافة علامات الجدولة إلى مجموعة فقرة من علامات الجدولة عبر خاصية "تنسيق الفقرة".
// 1 - أنشئ كائن "TabStop" ، ثم أضفه إلى المجموعة:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - قم بتمرير قيم خصائص علامة تبويب جديدة إلى طريقة "إضافة":
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// إضافة علامات الجدولة عند 5 سم لجميع الفقرات.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// كل حرف "علامة تبويب" يأخذ مؤشر المنشئ إلى موقع علامة الجدولة التالية.
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


