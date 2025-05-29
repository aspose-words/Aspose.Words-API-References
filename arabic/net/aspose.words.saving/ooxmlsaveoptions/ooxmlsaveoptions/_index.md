---
title: OoxmlSaveOptions
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ OoxmlSaveOptions لحفظ المستندات بسهولة بتنسيق Docx. تمتع بإدارة مستندات سلسة وتوافق مُحسّن.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيDocx تنسيق.

```csharp
public OoxmlSaveOptions()
```

## أمثلة

يوضح كيفية تعيين مواصفات توافق OOXML للمستند المحفوظ للالتزام بها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003،
// إدراج صورة سيؤدي إلى تحديد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO/IEC 29500:2008" أشكال VML.
// إذا قمنا بتعيين خاصية "التوافق" لكائن SaveOptions إلى "OoxmlCompliance.Iso29500_2008_Strict"،
 // أي مستند نقوم بحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// تحدد مستندنا المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### أنظر أيضا

* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## OoxmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيDocx ، Docm ،Dotx ،Dotm أو FlatOpc تنسيق.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن أن يكونDocx ،Docm ، Dotx ،Dotm أوFlatOpc . |

## أمثلة

يوضح كيفية دعم أحرف التحكم القديمة عند التحويل إلى .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// عندما نحفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريرها إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// اضبط خاصية "KeepLegacyControlChars" على "true" للحفاظ عليها
// حرف "ShortDateTime" القديم أثناء الحفظ.
// اضبط خاصية "KeepLegacyControlChars" على "false" لإزالة
// حرف "ShortDateTime" القديم من المستند الناتج.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
