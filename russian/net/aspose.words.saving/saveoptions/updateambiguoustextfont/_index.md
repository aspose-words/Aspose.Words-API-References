---
title: SaveOptions.UpdateAmbiguousTextFont
linktitle: UpdateAmbiguousTextFont
articleTitle: UpdateAmbiguousTextFont
second_title: Aspose.Words для .NET
description: Улучшите четкость текста в PDF-файлах с помощью UpdateAmbiguousTextFont. Обеспечьте точную визуализацию шрифтов на основе кодов символов для лучшей читаемости.
type: docs
weight: 150
url: /ru/net/aspose.words.saving/saveoptions/updateambiguoustextfont/
---
## SaveOptions.UpdateAmbiguousTextFont property

Определяет, будут ли изменяться атрибуты шрифта в соответствии с используемым кодом символа.

```csharp
public bool UpdateAmbiguousTextFont { get; set; }
```

## Примеры

Показывает, как обновить шрифт в соответствии с используемым кодом символа.

```csharp
Document doc = new Document(MyDir + "Special symbol.docx");
Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Ариал

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateAmbiguousTextFont = true;
doc.Save(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.UpdateAmbiguousTextFont.docx");
run = doc.FirstSection.Body.FirstParagraph.Runs[0];
Console.WriteLine(run.Text); // ฿
Console.WriteLine(run.Font.Name); // Ангсана Нью
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
