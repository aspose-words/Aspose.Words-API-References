---
title: OdtSaveOptions.OdtSaveOptions
second_title: Aspose.Words لمراجع .NET API
description: OdtSaveOptions البناء. تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ مستند في ملفOdt التنسيق.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ مستند في ملفOdt التنسيق.

```csharp
public OdtSaveOptions()
```

### أمثلة

يوضح كيفية جعل المستند المحفوظ يتوافق مع مخطط ODT الأقدم.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### أنظر أيضا

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../odtsaveoptions/)
* المجسم [Aspose.Words](../../../)

---

## OdtSaveOptions(string) {#constructor_2}

تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ مستند في ملفOdt format مشفر بكلمة مرور.

```csharp
public OdtSaveOptions(string password)
```

### أنظر أيضا

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../odtsaveoptions/)
* المجسم [Aspose.Words](../../../)

---

## OdtSaveOptions(SaveFormat) {#constructor_1}

تهيئة مثيل جديد لهذه الفئة يمكن استخدامه لحفظ مستند في ملفOdt أو Ott التنسيق.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن ان يكونOdt أوOtt. |

### أمثلة

يوضح كيفية تشفير مستند ODT/OTT المحفوظ بكلمة مرور، ثم تحميله باستخدام Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء OdtSaveOptions جديد، وقم بتمرير إما "SaveFormat.Odt"،
 // أو "SaveFormat.Ott" كتنسيق لحفظ المستند به.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// إذا فتحنا هذه الوثيقة باستخدام المحرر المناسب،
// سيطالبنا بكلمة المرور التي حددناها في كائن SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// إذا أردنا فتح هذا المستند أو تحريره مرة أخرى باستخدام Aspose.Words،
// سيتعين علينا توفير كائن LoadOptions بكلمة المرور الصحيحة لمنشئ التحميل.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../odtsaveoptions/)
* المجسم [Aspose.Words](../../../)


