---
title: OdtSaveOptions.Password
second_title: Aspose.Words لمراجع .NET API
description: OdtSaveOptions ملكية. الحصول على أو تعيين كلمة مرور لتشفير المستند.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

الحصول على أو تعيين كلمة مرور لتشفير المستند.

```csharp
public string Password { get; set; }
```

### ملاحظات

لحفظ المستند بدون تشفير ، يجب أن تكون هذه الخاصية خالية أو سلسلة فارغة.

### أمثلة

يوضح كيفية تشفير مستند ODT / OTT محفوظ بكلمة مرور ، ثم تحميله باستخدام Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء OdtSaveOptions جديد ، وقم بتمرير إما "SaveFormat.Odt" ،
// أو "SaveFormat.Ott" كتنسيق لحفظ المستند بتنسيق. 
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// إذا فتحنا هذا المستند باستخدام محرر مناسب ،
// سيطلب منا كلمة المرور التي حددناها في كائن SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// إذا كنا نرغب في فتح هذا المستند أو تعديله مرة أخرى باستخدام Aspose.Words ،
// سيتعين علينا توفير كائن LoadOptions بكلمة المرور الصحيحة لمنشئ التحميل.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../odtsaveoptions/)
* المجسم [Aspose.Words](../../../)


