---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.CompressionLevel تعداد. مستوى الضغط لملفات OOXML في C#.
type: docs
weight: 4870
url: /ar/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

مستوى الضغط لملفات OOXML.

(ملفات DOCX وDOTX هي أرشيف ZIP داخليًا، وتتحكم هذه الخاصية في مستوى ضغط الأرشيف.

لاحظ أن ملف FlatOpc ليس أرشيف ZIP، وبالتالي، لا تؤثر هذه الخاصية على ملفات FlatOpc.)

```csharp
public enum CompressionLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | مستوى الضغط العادي. مستوى الضغط الافتراضي المستخدم بواسطة Aspose.Words. |
| Maximum | `1` | الحد الأقصى لمستوى الضغط. |
| Fast | `2` | مستوى ضغط سريع. |
| SuperFast | `3` | مستوى ضغط فائق السرعة. يستخدم Microsoft Word مستوى الضغط هذا. |

## أمثلة

يوضح كيفية تحديد مستوى الضغط المطلوب استخدامه أثناء حفظ مستند OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// عندما نحفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريره إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// اضبط خاصية "CompressionLevel" على "CompressionLevel.Maximum" لتطبيق الضغط الأقوى والأبطأ.
// قم بتعيين خاصية "CompressionLevel" على "CompressionLevel.Normal" ليتم تطبيقها
// الضغط الافتراضي الذي يستخدمه Aspose.Words أثناء حفظ مستندات OOXML.
// اضبط خاصية "CompressionLevel" على "CompressionLevel.Fast" لتطبيق ضغط أسرع وأضعف.
// قم بتعيين خاصية "CompressionLevel" على "CompressionLevel.SuperFast" لتطبيقها
// الضغط الافتراضي الذي يستخدمه Microsoft Word.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
