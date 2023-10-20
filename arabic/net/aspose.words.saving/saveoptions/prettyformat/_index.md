---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words لـ .NET
description: SaveOptions PrettyFormat ملكية. متىحقيقي إخراج تنسيقات جميلة حيثما ينطبق ذلك. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

متى`حقيقي`، إخراج تنسيقات جميلة حيثما ينطبق ذلك. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool PrettyFormat { get; set; }
```

## ملاحظات

ضبط ل`حقيقي` لجعل مخرجات HTML وMHTML وEPUB وWordML وRTF وDOCX وODT قابلة للقراءة البشرية. مفيد للاختبار أو تصحيح الأخطاء.

## أمثلة

يوضح كيفية تحسين إمكانية قراءة التعليمات البرمجية الأولية لمستند html محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// يؤدي تمكين التنسيق الجميل إلى جعل تعليمات HTML البرمجية الأولية أكثر قابلية للقراءة عن طريق إضافة علامة جدولة وأحرف سطر جديدة.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");

if (usePrettyFormat)
    Assert.AreEqual(
        "<html>\r\n" +
                    "\t<head>\r\n" +
                        "\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\r\n" +
                        "\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\r\n" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />\r\n" +
                        "\t\t<title>\r\n" +
                        "\t\t</title>\r\n" +
                    "\t</head>\r\n" +
                    "\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\r\n" +
                        "\t\t<div>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span>Hello world!</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                        "\t\t</div>\r\n" +
                    "\t</body>\r\n</html>", 
        html);
else
    Assert.AreEqual(
        "<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />" +
                "<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
                $"<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" /><title></title></head>" +
                "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
                "<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>", 
        html);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
