---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OoxmlSaveOptions CompressionLevel لتحسين حفظ المستندات باستخدام مستويات ضغط قابلة للتخصيص لتحسين الأداء.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

يحدد مستوى الضغط المستخدم لحفظ المستند. القيمة الافتراضية هيNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
