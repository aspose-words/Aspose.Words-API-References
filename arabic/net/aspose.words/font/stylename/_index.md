---
title: StyleName
second_title: Aspose.Words لمراجع .NET API
description: الحصول على اسم نمط الحرف المطبق على هذا التنسيق أو تعيينه.
type: docs
weight: 420
url: /ar/net/aspose.words/font/stylename/
---
## Font.StyleName property

الحصول على اسم نمط الحرف المطبق على هذا التنسيق أو تعيينه.

```csharp
public string StyleName { get; set; }
```

### أمثلة

يوضح كيفية تغيير نمط النص الموجود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان للإشارة إلى الأنماط.
// 1 - استخدام اسم النمط:
builder.Font.StyleName = "Emphasis";
builder.Writeln("Text originally in \"Emphasis\" style");

// 2 - استخدام معرّف نمط مضمن:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// تحويل جميع استخدامات نمط إلى آخر ،
// باستخدام الأساليب المذكورة أعلاه للإشارة إلى الأنماط القديمة والجديدة.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    if (run.Font.StyleName == "Emphasis")
        run.Font.StyleName = "Strong";

    if (run.Font.StyleIdentifier == StyleIdentifier.IntenseEmphasis)
        run.Font.StyleIdentifier = StyleIdentifier.Strong;
}

doc.Save(ArtifactsDir + "Font.ChangeStyle.docx");
```

### أنظر أيضا

* class [Font](../../font)
* مساحة الاسم [Aspose.Words](../../font)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->