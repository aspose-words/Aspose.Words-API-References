---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StyleIdentifier المستقلة عن الإعدادات المحلية للأنماط المضمنة. حسّن مشاريعك بحلول تنسيق متسقة ومتعددة الاستخدامات.
type: docs
weight: 180
url: /ar/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

يحصل على معرف النمط المستقل عن الإعدادات المحلية للنمط المضمن.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## ملاحظات

بالنسبة للأنماط المحددة من قبل المستخدم (المخصصة)، تُرجع هذه الخاصيةUser.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
