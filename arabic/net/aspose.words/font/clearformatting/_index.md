---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words لـ .NET
description: استعد نصك إلى نمطه الأصلي باستخدام طريقة Font ClearFormatting. استمتع بتنسيق أنيق ومتناسق لمظهر أنيق!
type: docs
weight: 560
url: /ar/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

إعادة التعيين إلى تنسيق الخط الافتراضي.

```csharp
public void ClearFormatting()
```

## ملاحظات

يزيل كل تنسيقات الخطوط المحددة صراحةً على الكائن from which [`Font`](../) تم الحصول على تنسيق الخط بحيث يتم توريثه من الوالد المناسب.

## أمثلة

يوضح كيفية إدراج حقل ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

//أدرج ارتباطًا تشعبيًا وأبرزه باستخدام التنسيق المخصص.
// سيكون الرابط التشعبي عبارة عن جزء نصي قابل للنقر والذي سيأخذنا إلى الموقع المحدد في عنوان URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com"، خطأ);
builder.Font.ClearFormatting();
builder.Writeln(".");

// الضغط على Ctrl + النقر بزر الماوس الأيسر على الرابط الموجود في النص في Microsoft Word سيأخذنا إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
