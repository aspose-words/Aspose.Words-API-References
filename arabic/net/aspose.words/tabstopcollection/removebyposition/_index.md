---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words لـ .NET
description: TabStopCollection RemoveByPosition طريقة. إزالة علامة الجدولة عند الموضع المحدد من المجموعة في C#.
type: docs
weight: 120
url: /ar/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

إزالة علامة الجدولة عند الموضع المحدد من المجموعة.

```csharp
public void RemoveByPosition(double position)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| position | Double | موضع علامة التبويب (بالنقاط) المراد إزالتها. |

## أمثلة

يوضح كيفية تعديل موضع علامة التبويب اليمنى في الفقرات ذات الصلة بجدول المحتويات.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// التكرار خلال جميع الفقرات باستخدام أنماط جدول المحتويات المستندة إلى النتائج; هذا هو أي نمط بين TOC وTOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // احصل على علامة التبويب الأولى المستخدمة في هذه الفقرة، ويجب أن تكون هذه هي علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // استبدل علامة التبويب الافتراضية الأولى، وتوقف بعلامة جدولة مخصصة.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### أنظر أيضا

* class [TabStopCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
