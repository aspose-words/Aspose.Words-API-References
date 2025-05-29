---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font LocaleIdFarEast لإدارة معرفات الإعدادات المحلية بسهولة للأحرف الآسيوية المنسقة، مما يعزز تطبيقاتك متعددة اللغات.
type: docs
weight: 220
url: /ar/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

يحصل على معرف الإعدادات المحلية (اللغة) للأحرف الآسيوية المنسقة أو يعينه.

```csharp
public int LocaleIdFarEast { get; set; }
```

## ملاحظات

للحصول على قائمة بمعرفات الإعدادات المحلية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

## أمثلة

يوضح كيفية إدراج النص وتنسيقه في لغة الشرق الأقصى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد إعدادات الخط التي سيطبقها منشئ المستند على أي نص يقوم بإدراجه.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// قم بتسمية "FarEast" المكافئة للخط والإعدادات المحلية لدينا.
// إذا قام المنشئ بإدراج أحرف آسيوية باستخدام تكوين الخط هذا، فكل تشغيل يحتوي على
// سيتم عرض هذه الأحرف باستخدام الخط/الإعدادات المحلية "FarEast" بدلاً من الخط الافتراضي.
// قد يكون هذا مفيدًا عندما لا يحتوي الخط الغربي على تمثيلات مثالية للأحرف الآسيوية.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

//سيتم عرض هذا النص بالخط/الإعدادات المحلية الافتراضية.
builder.Writeln("Hello world!");

// نظرًا لأن هذه أحرف آسيوية، فسوف يتم تطبيق ما يعادلها من خطوط/إعدادات محلية في "FarEast" في هذه العملية.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
