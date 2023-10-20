---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words لـ .NET
description: DocumentBuilder PopFont طريقة. استرداد تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس في C#.
type: docs
weight: 590
url: /ar/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

استرداد تنسيق الأحرف الذي تم حفظه مسبقًا على المكدس.

```csharp
public void PopFont()
```

## أمثلة

يوضح كيفية استخدام مكدس التنسيق الخاص بمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط التشعبي.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// الحفاظ على تكوين التنسيق الحالي لدينا على المكدس.
builder.PushFont();

// قم بتغيير التنسيق الحالي للمنشئ من خلال تطبيق نمط جديد.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com"، خطأ);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// استعادة تنسيق الخط الذي حفظناه سابقًا وإزالة العنصر من المكدس.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### أنظر أيضا

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
