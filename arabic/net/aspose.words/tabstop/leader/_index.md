---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words لـ .NET
description: TabStop Leader ملكية. الحصول على أو تعيين نوع السطر الرئيسي المعروض أسفل حرف علامة التبويب في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

الحصول على أو تعيين نوع السطر الرئيسي المعروض أسفل حرف علامة التبويب.

```csharp
public TabLeader Leader { get; set; }
```

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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
