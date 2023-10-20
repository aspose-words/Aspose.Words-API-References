---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FontConfigSubstitutionRule فصل. قاعدة استبدال تكوين الخط في C#.
type: docs
weight: 2890
url: /ar/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

قاعدة استبدال تكوين الخط.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## الخصائص

| اسم | وصف |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | يحدد ما إذا كانت القاعدة مفعلة أم لا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | تحقق مما إذا كانت الأداة المساعدة لتكوين الخطوط متاحة أم لا. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | إعادة تعيين ذاكرة التخزين المؤقت لنتائج استدعاء Fontconfig. |

## ملاحظات

تستخدم هذه القاعدة الأداة المساعدة Fontconfig على أنظمة Linux (والأنظمة الأخرى المشابهة لـ Unix) للحصول على البديل إذا لم يكن الخط الأصلي متاحًا.

إذا لم تكن الأداة المساعدة لتكوين الخطوط متاحة، فسيتم تجاهل هذه القاعدة.

## أمثلة

يعرض استبدال تكوين الخط المعتمد على نظام التشغيل.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// يعمل كائن FontConfigSubstitutionRule بشكل مختلف على الأنظمة الأساسية التي تعمل بنظام Windows/غير Windows.
// على نظام التشغيل Windows، فهو غير متوفر.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// على Linux/Mac، سيكون لدينا إمكانية الوصول إليه وسنكون قادرين على تنفيذ العمليات.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### أنظر أيضا

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
