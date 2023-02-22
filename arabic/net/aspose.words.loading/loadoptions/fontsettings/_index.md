---
title: LoadOptions.FontSettings
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. يسمح بتحديد إعدادات خط الوثيقة.
type: docs
weight: 70
url: /ar/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

يسمح بتحديد إعدادات خط الوثيقة.

```csharp
public FontSettings FontSettings { get; set; }
```

### ملاحظات

عند تحميل بعض التنسيقات ، قد يطلب Aspose.Words حل الخطوط. على سبيل المثال ، عند تحميل مستندات HTML ، قد يقوم Aspose.Words بحل الخطوط لإجراء احتياطي للخط.

إذا تم التعيين على قيمة خالية ، فسيتم تعيين إعدادات الخط الثابت الافتراضية[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) سوف يستخدم.

القيمه الافتراضيه فارغه.

### أمثلة

يوضح كيفية تطبيق إعدادات استبدال الخط أثناء تحميل مستند.

```csharp
// قم بإنشاء كائن FontSettings ليحل محل الخط "Times New Roman"
// مع الخط "Arvo" من مجلد "MyFonts" الخاص بنا.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// تعيين هذا الكائن FontSettings كخاصية لكائن LoadOptions تم إنشاؤه حديثًا.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// قم بتحميل المستند ، ثم عرضه كملف PDF مع استبدال الخط.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

يوضح كيفية تعيين بدائل الخط أثناء التحميل.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// تعيين قاعدة استبدال الخط لكائن LoadOptions.
// إذا كان المستند الذي نقوم بتحميله يستخدم خطًا ليس لدينا ،
// ستستبدل هذه القاعدة الخط غير المتاح بآخر موجود.
// في هذه الحالة ، ستتحول جميع استخدامات "MissingFont" إلى "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", new[] {"Comic Sans MS"});

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// في هذه المرحلة ، سيظل هذا النص موجودًا في "MissingFont".
// سيحدث استبدال الخط عندما نعرض المستند.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### أنظر أيضا

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


