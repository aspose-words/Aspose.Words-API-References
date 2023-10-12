---
title: OdtSaveOptions.SaveFormat
second_title: Aspose.Words لمراجع .NET API
description: OdtSaveOptions ملكية. يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكونOdt أوOtt .
type: docs
weight: 50
url: /ar/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكونOdt أوOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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


