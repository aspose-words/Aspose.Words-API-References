---
title: Font.StyleIdentifier
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين معرف النمط المستقل للإعدادات المحلية لنمط الحرف المطبق على هذا التنسيق.
type: docs
weight: 410
url: /ar/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

الحصول على أو تعيين معرف النمط المستقل للإعدادات المحلية لنمط الحرف المطبق على هذا التنسيق.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


