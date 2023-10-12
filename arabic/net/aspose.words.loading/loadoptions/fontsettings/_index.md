---
title: LoadOptions.FontSettings
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. يسمح بتحديد إعدادات خط المستند.
type: docs
weight: 60
url: /ar/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

يسمح بتحديد إعدادات خط المستند.

```csharp
public FontSettings FontSettings { get; set; }
```

### ملاحظات

عند تحميل بعض التنسيقات، قد يتطلب Aspose.Words حل الخطوط. على سبيل المثال، عند تحميل مستندات HTML، قد يقوم Aspose.Words بتحليل الخطوط لإجراء عملية احتياطية للخط.

إذا تم تعيينه على`باطل` ، إعدادات الخط الثابت الافتراضية[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) سوف يستخدم.

القيمة الافتراضية هي`باطل`.

### أمثلة

يوضح كيفية تطبيق إعدادات استبدال الخط أثناء تحميل مستند.

```csharp
// قم بإنشاء كائن FontSettings الذي سيحل محل الخط "Times New Roman".
// بالخط "Arvo" من مجلد "MyFonts" الخاص بنا.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// قم بتعيين كائن FontSettings كخاصية لكائن LoadOptions المنشأ حديثًا.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// قم بتحميل المستند، ثم قم بعرضه كملف PDF مع استبدال الخط.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

يوضح كيفية تعيين بدائل الخطوط أثناء التحميل.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// قم بتعيين قاعدة استبدال الخط لكائن LoadOptions.
// إذا كان المستند الذي نقوم بتحميله يستخدم خطًا غير متوفر لدينا،
// ستستبدل هذه القاعدة الخط غير المتوفر بخط موجود.
// في هذه الحالة، سيتم تحويل جميع استخدامات "MissingFont" إلى "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", new[] {"Comic Sans MS"});

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// عند هذه النقطة، سيظل هذا النص موجودًا في "MissingFont".
// سيتم استبدال الخط عندما نعرض المستند.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### أنظر أيضا

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


