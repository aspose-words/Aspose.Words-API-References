---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words для .NET
description: Узнайте, как свойство UseTargetMachineFonts в HtmlFixedSaveOptions улучшает отображение документа, используя шрифты целевой машины. Оптимизируйте управление шрифтами сегодня!
type: docs
weight: 210
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

Флаг указывает, должны ли использоваться шрифты с целевой машины для отображения документа. Если этот флаг установлен в`истинный` ,[`FontFormat`](../fontformat/) и[`ExportEmbeddedFonts`](../exportembeddedfonts/) свойства не имеют эффекта, также[`ResourceSavingCallback`](../resourcesavingcallback/) не запускается для шрифтов. По умолчанию`ЛОЖЬ` .

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## Примеры

Показывает, как использовать шрифты только с целевого компьютера при сохранении документа в формате HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
