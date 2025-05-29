---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words для .NET
description: Улучшите свой вывод с помощью свойства PrettyFormat SaveOptions. Активируйте для получения более чистых, хорошо структурированных результатов. Значение по умолчанию — false. Почувствуйте разницу!
type: docs
weight: 110
url: /ru/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Когда`истинный` , красивые форматы вывода, где это применимо. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool PrettyFormat { get; set; }
```

## Примечания

Установить на`истинный` для того, чтобы сделать выходные данные HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемыми. Полезно для тестирования или отладки.

## Примеры

Показывает, как улучшить читаемость исходного кода сохраненного .html-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Включение красивого форматирования делает необработанный HTML-код более читабельным за счет добавления табуляции и символов новой строки.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");
string newLine = Environment.NewLine;

if (usePrettyFormat)
    Assert.AreEqual(
        $"<html>{newLine}" +
                    $"\t<head>{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />{newLine}" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />{newLine}" +
                        $"\t\t<title>{newLine}" +
                        $"\t\t</title>{newLine}" +
                    $"\t</head>{newLine}" +
                    $"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">{newLine}" +
                        $"\t\t<div>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span>Hello world!</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                        $"\t\t</div>{newLine}" +
                    $"\t</body>{newLine}</html>", 
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

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
