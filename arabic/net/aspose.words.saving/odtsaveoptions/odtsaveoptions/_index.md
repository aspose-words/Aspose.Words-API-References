---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ OdtSaveOptions لحفظ المستندات بتنسيق ODT بسهولة. بسّط سير عملك مع هذه الأداة الفعّالة!
type: docs
weight: 10
url: /ar/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيOdt تنسيق.

```csharp
public OdtSaveOptions()
```

## أمثلة

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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيOdt format مشفر بكلمة مرور.

```csharp
public OdtSaveOptions(string password)
```

### أنظر أيضا

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند فيOdt أو Ott تنسيق.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| saveFormat | SaveFormat | يمكن أن يكونOdt أوOtt. |

## أمثلة

يوضح كيفية تشفير مستند ODT/OTT المحفوظ بكلمة مرور، ثم تحميله باستخدام Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء OdtSaveOptions جديد، ثم مرر إما "SaveFormat.Odt" أو
 // أو "SaveFormat.Ott" كتنسيق لحفظ المستند فيه.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// إذا فتحنا هذا المستند باستخدام محرر مناسب،
// سيطلب منا إدخال كلمة المرور التي حددناها في كائن SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// إذا أردنا فتح أو تحرير هذا المستند مرة أخرى باستخدام Aspose.Words،
// سيتعين علينا توفير كائن LoadOptions بكلمة المرور الصحيحة لمنشئ التحميل.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
