---
title: Font.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font StyleIdentifier لإدارة أنماط الأحرف في تنسيقك بسهولة. حسّن تصميمك بحلول مستقلة عن الإعدادات المحلية!
type: docs
weight: 420
url: /ar/net/aspose.words/font/styleidentifier/
---
## Font.StyleIdentifier property

يحصل على أو يعين معرف النمط المستقل عن الإعدادات المحلية لنمط الأحرف المطبق على هذا التنسيق.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## أمثلة

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

// تحويل جميع استخدامات نمط واحد إلى نمط آخر،
// استخدام الأساليب المذكورة أعلاه للإشارة إلى الأنماط القديمة والجديدة.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
