---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words لـ .NET
description: اكتشف خصائص TabStop Leader لتخصيص أنواع خطوط الدليل لعلامات التبويب لديك، مما يُحسّن وضوح مستنداتك وعرضها. حسّن تنسيقك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

يحصل على نوع الخط الرئيسي المعروض أسفل حرف التبويب أو يعينه.

```csharp
public TabLeader Leader { get; set; }
```

## أمثلة

يوضح كيفية تعديل موضع علامة التبويب اليمنى في الفقرات ذات الصلة بجدول المحتويات.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// قم بالتكرار خلال جميع الفقرات باستخدام أنماط تعتمد على نتائج جدول المحتويات; وهذا هو أي نمط بين جدول المحتويات وجدول المحتويات 9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // احصل على علامة التبويب الأولى المستخدمة في هذه الفقرة، ويجب أن تكون هذه هي علامة التبويب المستخدمة لمحاذاة أرقام الصفحات.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // استبدال علامة التبويب الافتراضية الأولى، والتوقف بعلامة تبويب مخصصة.
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
