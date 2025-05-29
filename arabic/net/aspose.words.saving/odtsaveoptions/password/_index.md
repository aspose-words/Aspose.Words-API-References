---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: أمّن مستنداتك باستخدام خاصية كلمة المرور في OdtSaveOptions. يمكنك بسهولة تعيين كلمة مرور أو استردادها لضمان تشفير قوي وحماية بيانات مُحسّنة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

يحصل على كلمة مرور لتشفير المستند أو يعينها.

```csharp
public string Password { get; set; }
```

## ملاحظات

لحفظ المستند بدون تشفير يجب أن تكون هذه الخاصية`باطل` أو سلسلة فارغة.

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

* class [OdtSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
