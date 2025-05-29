---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words для .NET
description: Управляйте поведением гиперссылок в вашем PDF с помощью PdfSaveOptions. Легко настройте ссылки на открытие в новом окне или вкладке для улучшения пользовательского опыта.
type: docs
weight: 230
url: /ru/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Возвращает или задает значение, определяющее, будут ли гиперссылки в выходном документе PDF принудительно открываться в новом окне (или вкладке) браузера.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` . Когда это значение установлено на`истинный` гиперссылки сохраняются с помощью кода JavaScript. код JavaScript`app.launchURL("URL", true);` , где`URL` является гиперссылкой.

Обратите внимание, что если этот параметр установлен на`истинный` гиперссылки не работают в некоторых программах для чтения PDF-файлов, например Chrome, Firefox.

Действия JavaScript запрещены стандартами PDF/A-1 и PDF/A-2.`ЛОЖЬ`будет использоваться автоматически при сохранении в формате PDF/A-1 и PDF/A-2.

## Примеры

Показывает, как сохранять гиперссылки в документе, конвертируемом в PDF, чтобы при нажатии на них открывались новые страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "OpenHyperlinksInNewWindow" в значение "true", чтобы сохранить все гиперссылки с помощью кода Javascript
// что заставляет читателей открывать эти ссылки в новых окнах/вкладках браузера.
// Установите свойство "OpenHyperlinksInNewWindow" в значение "false", чтобы сохранить все гиперссылки в обычном режиме.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
