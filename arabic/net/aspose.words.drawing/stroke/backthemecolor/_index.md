---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words لـ .NET
description: خصّص تصميمك باستخدام خاصية Stroke BackThemeColor. حدّد بسهولة لونًا لخلفية حدودك لتحسين مظهرها.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون خلفية الحد.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

## أمثلة

يوضح كيفية ضبط لون السمة والصبغة والظل.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### أنظر أيضا

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
