---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة StreamFontSource OpenFontDataStream للوصول بكفاءة إلى تدفقات بيانات الخطوط عند الطلب، مما يعزز سير عمل التصميم الخاص بك.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

يجب أن تفتح هذه الطريقة التدفق ببيانات الخط عند الطلب.

```csharp
public abstract Stream OpenFontDataStream()
```

### قيمة الإرجاع

دفق بيانات الخط.

## ملاحظات

سيتم إغلاق الدفق بعد القراءة. لا حاجة لإغلاقه صراحةً.

## أمثلة

يوضح كيفية تحميل الخطوط من الدفق.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// قم بتحميل بيانات الخط فقط عند الحاجة إليها بدلاً من تخزينها في الذاكرة
/// طوال عمر كائن "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### أنظر أيضا

* class [StreamFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
