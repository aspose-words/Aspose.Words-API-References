---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.TabLeader، التي تحدد أنماط خطوط القيادة للعلامات التبويبية، مما يعزز تنسيق المستندات وقابليتها للقراءة في مشاريعك.
type: docs
weight: 7040
url: /ar/net/aspose.words/tableader/
---
## TabLeader enumeration

يحدد نوع الخط الرئيسي المعروض أسفل حرف التبويب.

```csharp
public enum TabLeader
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم عرض أي خط قائد. |
| Dots | `1` | يتكون الخط الرئيسي من نقاط. |
| Dashes | `2` | يتكون الخط الرئيسي من شرطات. |
| Line | `3` | الخط الرئيسي هو خط واحد. |
| Heavy | `4` | الخط الرئيسي عبارة عن خط سميك واحد. |
| MiddleDot | `5` | يتكون خط القائد من النقاط الوسطى. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
