---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetEffectiveTabStops لاسترداد كل علامات التبويب في فقرة، بما في ذلك تلك الموجودة في الأنماط والقوائم لتحسين التنسيق.
type: docs
weight: 270
url: /ar/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

إرجاع مجموعة من جميع علامات التبويب المطبقة على هذه الفقرة، بما في ذلك تلك المطبقة بشكل غير مباشر بواسطة الأنماط أو القوائم.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## أمثلة

يوضح كيفية تعيين علامات تبويب مخصصة لفقرة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// إذا كنا في فقرة لا تحتوي على علامات تبويب في هذه المجموعة،
// سوف يقفز المؤشر 36 نقطة في كل مرة نضغط فيها على مفتاح Tab في Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// يمكننا إضافة علامات تبويب مخصصة في Microsoft Word إذا قمنا بتمكين المسطرة عبر علامة التبويب "عرض".
// كل وحدة على هذه المسطرة هي علامتي تبويب افتراضيتين، أي 72 نقطة.
//يمكننا إضافة علامات تبويب مخصصة برمجيًا مثل هذا.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// يمكننا رؤية علامات التبويب هذه في Microsoft Word عن طريق تمكين المسطرة عبر "عرض" -> "إظهار" -> "المسطرة".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// أي أحرف تبويب نضيفها ستستخدم علامات التبويب الموجودة على المسطرة وقد،
// اعتمادًا على قيمة قائد علامة التبويب، اترك خطًا بين وجهة المغادرة ووجهة الوصول في علامة التبويب.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### أنظر أيضا

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
