---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية محاذاة علامات التبويب لتخصيص محاذاة النص بسهولة عند علامات التبويب، مما يعزز تخطيط مستندك وقابليته للقراءة.
type: docs
weight: 20
url: /ar/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

يحصل على محاذاة النص عند علامة التبويب هذه أو يعينها.

```csharp
public TabAlignment Alignment { get; set; }
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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
