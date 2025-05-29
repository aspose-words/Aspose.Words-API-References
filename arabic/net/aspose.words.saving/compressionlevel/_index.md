---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.CompressionLevel لتحسين أحجام ملفات OOXML، وتعزيز الأداء والكفاءة في معالجة المستندات.
type: docs
weight: 5610
url: /ar/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

مستوى الضغط لملفات OOXML.

(ملفات DOCX وDOTX هي أرشيف ZIP داخليًا، تتحكم هذه الخاصية في مستوى ضغط الأرشيف.

لاحظ أن ملف FlatOpc ليس أرشيف ZIP، وبالتالي، لا تؤثر هذه الخاصية على ملفات FlatOpc.)

```csharp
public enum CompressionLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Normal | `0` | مستوى الضغط العادي. مستوى الضغط الافتراضي المستخدم في Aspose.Words. |
| Maximum | `1` | الحد الأقصى لمستوى الضغط. |
| Fast | `2` | مستوى ضغط سريع. |
| SuperFast | `3` | مستوى ضغط فائق السرعة. يستخدم مايكروسوفت وورد هذا المستوى من الضغط. |

## أمثلة

يوضح كيفية تحديد مستوى الضغط الذي يجب استخدامه أثناء حفظ مستند OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// عندما نحفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريرها إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// قم بضبط خاصية "CompressionLevel" على "CompressionLevel.Maximum" لتطبيق أقوى وأبطأ ضغط.
// اضبط خاصية "CompressionLevel" على "CompressionLevel.Normal" لتطبيقها
// الضغط الافتراضي الذي يستخدمه Aspose.Words أثناء حفظ مستندات OOXML.
// قم بضبط خاصية "CompressionLevel" إلى "CompressionLevel.Fast" لتطبيق ضغط أسرع وأضعف.
// اضبط خاصية "CompressionLevel" على "CompressionLevel.SuperFast" لتطبيقها
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
