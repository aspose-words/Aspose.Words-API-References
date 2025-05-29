---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية Font LocaleId تنسيق نصك من خلال إدارة مُعرّفات الإعدادات المحلية لمختلف لغات البرمجة. حسّن مهاراتك البرمجية اليوم!
type: docs
weight: 200
url: /ar/net/aspose.words/font/localeid/
---
## Font.LocaleId property

يحصل على معرف الإعدادات المحلية (اللغة) للأحرف المنسقة أو يعينه.

```csharp
public int LocaleId { get; set; }
```

## ملاحظات

للحصول على قائمة بمعرفات الإعدادات المحلية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

## أمثلة

يوضح كيفية تعيين موقع النص الذي نضيفه باستخدام منشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتعيين إعدادات الخط إلى اللغة الإنجليزية وأدرجنا بعض النصوص الروسية،
// لن يتعرف مدقق الإملاء المحلي باللغة الإنجليزية على النص ويكتشفه كخطأ إملائي.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// قم بتعيين إعدادات محلية مطابقة للنص الذي سنضيفه لتطبيق مدقق الإملاء المناسب.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
