---
title: Font.LocaleIdFarEast
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين المعرف المحلي اللغة للأحرف الآسيوية المنسقة.
type: docs
weight: 220
url: /ar/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

الحصول على أو تعيين المعرف المحلي (اللغة) للأحرف الآسيوية المنسقة.

```csharp
public int LocaleIdFarEast { get; set; }
```

### ملاحظات

للحصول على قائمة المعرفات المحلية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

### أمثلة

يوضح كيفية إدراج النص وتنسيقه بلغة الشرق الأقصى.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد إعدادات الخط التي سيطبقها منشئ المستندات على أي نص يقوم بإدراجه.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// قم بتسمية "FarEast" المكافئة للخط واللغة الخاصة بنا.
// إذا قام المنشئ بإدراج أحرف آسيوية بتكوين الخط هذا، فكل تشغيل يحتوي على
// ستعرض هذه الأحرف باستخدام الخط/اللغة المحلية "FarEast" بدلاً من الإعداد الافتراضي.
// قد يكون هذا مفيدًا عندما لا يحتوي الخط الغربي على تمثيل مثالي للأحرف الآسيوية.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// سيتم عرض هذا النص بالخط/اللغة الافتراضية.
builder.Writeln("Hello world!");

// نظرًا لأن هذه الأحرف آسيوية، فإن هذا التشغيل سيطبق مرادفات الخط/اللغة المحلية لـ "FarEast".
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


