---
title: OoxmlSaveOptions.OoxmlSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: OoxmlSaveOptions البناء. يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقDocx التنسيق .
type: docs
weight: 10
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقDocx التنسيق .

```csharp
public OoxmlSaveOptions()
```

### أمثلة

يوضح كيفية تعيين مواصفات توافق OOXML لمستند محفوظ للالتزام به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا قمنا بتكوين خيارات التوافق لتتوافق مع Microsoft Word 2003 ،
// إدراج صورة سيحدد شكلها باستخدام VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// لا يدعم معيار OOXML "ISO / IEC 29500: 2008" أشكال VML.
// إذا قمنا بتعيين خاصية "الامتثال" لكائن SaveOptions على "OoxmlCompliance.Iso29500_2008_Strict" ،
 // أي مستند نقوم بحفظه أثناء تمرير هذا الكائن يجب أن يتبع هذا المعيار.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// يحدد المستند المحفوظ الشكل باستخدام DML للالتزام بمعيار OOXML "ISO / IEC 29500: 2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### أنظر أيضا

* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* المجسم [Aspose.Words](../../../)

---

## OoxmlSaveOptions(SaveFormat) {#constructor_1}

يقوم بتهيئة مثيل جديد من هذه الفئة يمكن استخدامه لحفظ مستند بتنسيقDocx ، Docm وDotx وDotm أو FlatOpc التنسيق .

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن ان يكونDocx وDocm ، Dotx وDotm أوFlatOpc . |

### أمثلة

يوضح كيفية دعم أحرف التحكم القديمة عند التحويل إلى docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// عندما نحفظ المستند بتنسيق OOXML ، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريره إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// اضبط خاصية "KeepLegacyControlChars" على "true" للاحتفاظ بها
// الحرف القديم "ShortDateTime" أثناء الحفظ.
// اضبط خاصية "KeepLegacyControlChars" على "خطأ" لإزالتها
// الحرف القديم "ShortDateTime" من مستند الإخراج.
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
* مساحة الاسم [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


