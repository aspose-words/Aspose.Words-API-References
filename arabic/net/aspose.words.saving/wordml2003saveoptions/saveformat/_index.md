---
title: WordML2003SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُعرّف خاصية SaveFormat في WordML2003SaveOptions تنسيقات حفظ المستندات. تمتع بتوافق تام مع WordML لملفاتك!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/wordml2003saveoptions/saveformat/
---
## WordML2003SaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. لا يمكن أن يكون إلاWordML .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## أمثلة

يوضح كيفية إدارة المحتوى الخام للمستند الناتج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "WordML2003SaveOptions" لتمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية حفظ المستند إلى تنسيق حفظ WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// اضبط خاصية "PrettyFormat" على "true" لتطبيق مسافة بادئة لأحرف الجدولة و
//أسطر جديدة لجعل محتوى المستند الناتج الخام أسهل للقراءة.
// اضبط خاصية "PrettyFormat" على "false" لحفظ محتوى المستند الخام في نص واحد مستمر.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [WordML2003SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
