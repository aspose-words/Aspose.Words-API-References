---
title: Font.Style
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين نمط الأحرف المطبق على هذا التنسيق.
type: docs
weight: 400
url: /ar/net/aspose.words/font/style/
---
## Font.Style property

الحصول على أو تعيين نمط الأحرف المطبق على هذا التنسيق.

```csharp
public Style Style { get; set; }
```

### أمثلة

يطبق تسطيرًا مزدوجًا على كافة عمليات التشغيل في مستند تم تنسيقه باستخدام أنماط أحرف مخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل نمطًا مخصصًا وقم بتطبيقه على النص الذي تم إنشاؤه باستخدام أداة إنشاء المستندات.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// كرر كل عملية تشغيل وأضف تسطيرًا مزدوجًا إلى كل نمط مخصص.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
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
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


