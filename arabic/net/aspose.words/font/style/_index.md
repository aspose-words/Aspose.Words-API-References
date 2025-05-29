---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية نمط الخط لتخصيص أنماط الأحرف في التنسيق الخاص بك لتحسين جاذبية النص وسهولة قراءته.
type: docs
weight: 410
url: /ar/net/aspose.words/font/style/
---
## Font.Style property

يحصل على نمط الحرف المطبق على هذا التنسيق أو يعينه.

```csharp
public Style Style { get; set; }
```

## أمثلة

يتم تطبيق خط مزدوج على كافة التشغيلات في المستند المنسقة باستخدام أنماط الأحرف المخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج نمط مخصص وتطبيقه على النص الذي تم إنشاؤه باستخدام منشئ المستندات.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// كرر كل عملية تشغيل وأضف خطًا مزدوجًا إلى كل نمط مخصص.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### أنظر أيضا

* class [Style](../../style/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
