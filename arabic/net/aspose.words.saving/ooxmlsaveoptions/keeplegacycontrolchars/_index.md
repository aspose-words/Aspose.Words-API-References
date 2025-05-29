---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية KeepLegacyControlChars في OoxmlSaveOptions للحفاظ على التنسيق الأصلي لأحرف التحكم القديمة لتحويل المستندات بسلاسة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

يحتفظ بالتمثيل الأصلي لأحرف التحكم القديمة.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

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

* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
