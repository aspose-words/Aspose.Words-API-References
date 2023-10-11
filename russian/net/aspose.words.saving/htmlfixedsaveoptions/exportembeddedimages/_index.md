---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
second_title: Справочник по API Aspose.Words для .NET
description: HtmlFixedSaveOptions свойство. Указывает должны ли изображения быть встроены в HTMLдокумент в формате Base64. Обратите внимание что установка этого флага может значительно увеличить размер выходного HTMLфайла.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Указывает, должны ли изображения быть встроены в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### Примеры

Показывает, как определить, где хранить изображения при экспорте документа в HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Когда мы экспортируем документ со встроенными изображениями в .html,
// Aspose.Words может размещать изображения в двух возможных местах.
// Установка флага «ExportEmbeddedImages» в значение «true» сохранит необработанные данные
// для всех изображений в выходном HTML-документе в атрибуте "src" <image> теги.
// Установка этого флага в значение «false» создаст файл изображения в локальной файловой системе для каждого изображения,
// и сохраним все эти файлы в отдельной папке.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


