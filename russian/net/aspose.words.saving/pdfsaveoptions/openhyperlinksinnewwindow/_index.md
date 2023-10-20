---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words для .NET
description: PdfSaveOptions OpenHyperlinksInNewWindow свойство. Получает или задает значение определяющее будут ли гиперссылки в выходном PDFдокументе document принудительно открываться в новом окне или вкладке браузера на С#.
type: docs
weight: 230
url: /ru/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Получает или задает значение, определяющее, будут ли гиперссылки в выходном PDF-документе document принудительно открываться в новом окне (или вкладке) браузера.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` . Когда это значение установлено на`истинный` Гиперссылки сохраняются с использованием кода JavaScript. Код JavaScript `app.launchURL("URL", правда);` , где`URL-адрес` это гиперссылка.

Обратите внимание: если для этой опции установлено значение`истинный` гиперссылки не работают в некоторых программах для чтения PDF-файлов, например Chrome, Firefox.

Действия JavaScript запрещены стандартами PDF/A-1 и PDF/A-2.`ЛОЖЬ`будет использоваться автоматически при сохранении в PDF/A-1 и PDF/A-2.

## Примеры

Показывает, как сохранить гиперссылки в документе, который мы конвертируем в PDF, чтобы при нажатии на них открывались новые страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства OpenHyperlinksInNewWindow значение «true», чтобы сохранить все гиперссылки с использованием кода Javascript.
// это заставляет читателей открывать эти ссылки в новых вкладках Windows/браузера.
// Установите для свойства «OpenHyperlinksInNewWindow» значение «false», чтобы все гиперссылки сохранялись в обычном режиме.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
