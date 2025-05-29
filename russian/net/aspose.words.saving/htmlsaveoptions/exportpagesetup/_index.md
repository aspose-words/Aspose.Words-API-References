---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ExportPageSetup улучшает экспорт HTML, MHTML или EPUB, позволяя настраивать параметры страницы для лучшего вывода.
type: docs
weight: 220
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Примечания

Каждый[`Section`](../../../aspose.words/section/) в модели документа Aspose.Words предусмотрена информация о настройке страницы через[`PageSetup`](../../../aspose.words/pagesetup/) класс. При экспорте документа в формат HTML вам может потребоваться сохранить эту информацию для дальнейшего использования. В частности, настройка страницы может быть важна для рендеринга на страничном носителе (печати) или последующего преобразования в собственные форматы файлов Microsoft Word (DOCX, DOC, RTF, WML).

В большинстве случаев HTML предназначен для просмотра в браузерах, где не выполняется пагинация. Поэтому эта функция по умолчанию неактивна.

## Примеры

Показывает, как решить, следует ли сохранять структуру раздела/информацию о настройках страницы при сохранении в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, следует ли сохранить или отменить настройки страницы.
// Если мы установим флаг «ExportPageSetup» на «true», выходной HTML-документ будет содержать нашу конфигурацию настроек страницы.
// Если мы установим флаг "ExportPageSetup" на "false", операция сохранения отменит наши настройки страницы
// для первого раздела, и оба раздела будут выглядеть одинаково.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
