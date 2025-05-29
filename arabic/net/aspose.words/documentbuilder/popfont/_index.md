---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة DocumentBuilder PopFont لاستعادة تنسيق الأحرف بسهولة من المكدس، مما يعزز عملية إنشاء المستندات الخاصة بك.
type: docs
weight: 630
url: /ar/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

يسترجع تنسيق الأحرف المحفوظ مسبقًا على المكدس.

```csharp
public void PopFont()
```

## أمثلة

يوضح كيفية استخدام مجموعة التنسيق الخاصة بمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإعداد تنسيق الخط، ثم اكتب النص الذي يسبق الارتباط التشعبي.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

//الحفاظ على تكوين التنسيق الحالي على المكدس.
builder.PushFont();

// تغيير تنسيق المنشئ الحالي من خلال تطبيق نمط جديد.
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
