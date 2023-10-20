---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words لـ .NET
description: Font LocaleId ملكية. الحصول على أو تعيين المعرف المحلي اللغة للأحرف المنسقة في C#.
type: docs
weight: 200
url: /ar/net/aspose.words/font/localeid/
---
## Font.LocaleId property

الحصول على أو تعيين المعرف المحلي (اللغة) للأحرف المنسقة.

```csharp
public int LocaleId { get; set; }
```

## ملاحظات

للحصول على قائمة المعرفات المحلية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

## أمثلة

يوضح كيفية تعيين لغة النص الذي نضيفه باستخدام أداة إنشاء المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتعيين لغة الخط على اللغة الإنجليزية وأدخلنا بعض النصوص الروسية،
// لن يتعرف المدقق الإملائي للغة الإنجليزية على النص ويكتشفه كخطأ إملائي.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// قم بتعيين لغة مطابقة للنص الذي نحن على وشك إضافته لتطبيق المدقق الإملائي المناسب.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
