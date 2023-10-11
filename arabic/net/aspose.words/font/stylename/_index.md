---
title: Font.StyleName
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين اسم نمط الأحرف المطبق على هذا التنسيق.
type: docs
weight: 420
url: /ar/net/aspose.words/font/stylename/
---
## Font.StyleName property

الحصول على أو تعيين اسم نمط الأحرف المطبق على هذا التنسيق.

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

// 2 - استخدام معرف النمط المدمج:
builder.Font.StyleIdentifier = StyleIdentifier.IntenseEmphasis;
builder.Writeln("Text originally in \"Intense Emphasis\" style");

// تحويل كافة الاستخدامات من نمط إلى آخر،
// استخدام الطرق المذكورة أعلاه للإشارة إلى الأنماط القديمة والجديدة.
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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


