---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words для .NET
description: Оптимизируйте свой HTML с помощью свойства HtmlSaveOptions ExportXhtmlTransitional. Управляйте объявлениями DOCTYPE для лучшей совместимости в форматах HTML, MHTML и EPUB.
type: docs
weight: 280
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Указывает, следует ли записывать декларацию DOCTYPE при сохранении в HTML или MHTML. Когда`истинный` , записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию:`ЛОЖЬ`. При сохранении в формате EPUB или HTML5 (Html5 ) всегда записывается декларация DOCTYPE .

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Примечания

Aspose.Words всегда записывает правильно сформированный HTML независимо от этой настройки.

Когда`истинный`, начало выходного HTML-документа будет выглядеть так:

Aspose.Words стремится выводить XHTML в соответствии со спецификацией XHTML 1.0 Transitional, , но вывод не всегда будет соответствовать DTD. Некоторые структуры внутри документа Microsoft Word трудно или невозможно сопоставить с документом, который будет соответствовать схеме XHTML. Например, XHTML не допускает вложенных списков (UL не может быть вложен в другой элемент UL), , но в документе Microsoft Word многоуровневые списки встречаются довольно часто.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

## Примеры

Показывает, как отображать заголовок DOCTYPE при преобразовании документов в переходный стандарт Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Наш документ будет содержать заголовок декларации DOCTYPE только в том случае, если мы установили флаг «ExportXhtmlTransitional» в значение «true».
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
