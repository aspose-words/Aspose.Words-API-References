---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words لـ .NET
description: خصّص إعدادات خط مستندك باستخدام LoadOptions FontSettings لتحسين سهولة القراءة والأسلوب. حسّن مستنداتك بسهولة!
type: docs
weight: 60
url: /ar/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

يسمح بتحديد إعدادات خط المستند.

```csharp
public FontSettings FontSettings { get; set; }
```

## ملاحظات

عند تحميل بعض التنسيقات، قد يتطلب Aspose.Words تحليل الخطوط. على سبيل المثال، عند تحميل مستندات HTML، قد يقوم Aspose.Words بتحليل الخطوط لإجراء عملية الرجوع إلى الخلف.

إذا تم ضبطه على`باطل` ، إعدادات الخط الثابت الافتراضية[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) سيتم استخدامها.

القيمة الافتراضية هي`باطل`.

## أمثلة

يوضح كيفية تطبيق إعدادات استبدال الخط أثناء تحميل المستند.

```csharp
// قم بإنشاء كائن FontSettings الذي سيحل محل الخط "Times New Roman"
// باستخدام الخط "Arvo" من مجلد "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// قم بتعيين كائن FontSettings هذا كخاصية لكائن LoadOptions الذي تم إنشاؤه حديثًا.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// قم بتحميل المستند، ثم قم بتقديمه كملف PDF مع استبدال الخط.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

يوضح كيفية تحديد بدائل الخطوط أثناء التحميل.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// تعيين قاعدة استبدال الخط لكائن LoadOptions.
// إذا كانت الوثيقة التي نقوم بتحميلها تستخدم خطًا غير موجود لدينا،
// هذه القاعدة سوف تحل محل الخط غير المتوفر بخط موجود.
// في هذه الحالة، سيتم تحويل جميع استخدامات "MissingFont" إلى "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// في هذه المرحلة، سيظل النص في "MissingFont".
// سوف يتم استبدال الخط عندما نقوم بعرض المستند.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### أنظر أيضا

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
