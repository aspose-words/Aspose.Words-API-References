---
title: Font.StyleName
linktitle: StyleName
articleTitle: StyleName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font StyleName، وقم بإدارة أنماط الأحرف بسهولة لتحسين تنسيق النص ومرونة التصميم في مشاريعك.
type: docs
weight: 430
url: /ar/net/aspose.words/font/stylename/
---
## Font.StyleName property

يحصل على اسم نمط الحرف المطبق على هذا التنسيق أو يعينه.

```csharp
public string StyleName { get; set; }
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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
