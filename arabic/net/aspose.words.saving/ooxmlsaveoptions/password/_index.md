---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: OoxmlSaveOptions Password ملكية. الحصول على/تعيين كلمة مرور لتشفير المستند باستخدام خوارزمية التشفير القياسية ECMA376 في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

الحصول على/تعيين كلمة مرور لتشفير المستند باستخدام خوارزمية التشفير القياسية ECMA376.

```csharp
public string Password { get; set; }
```

## ملاحظات

من أجل حفظ المستند بدون تشفير، يجب أن تكون هذه الخاصية`باطل` أو سلسلة فارغة.

## أمثلة

يوضح كيفية إنشاء مستند Office Open XML مشفر بكلمة مرور.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// لن نتمكن من فتح هذا المستند باستخدام Microsoft Word أو
// Aspose.Words دون توفير كلمة المرور الصحيحة.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// افتح المستند المشفر عن طريق تمرير كلمة المرور الصحيحة في كائن LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
