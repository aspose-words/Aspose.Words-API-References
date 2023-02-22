---
title: PdfSaveOptions.DisplayDocTitle
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Флаг указывающий должен ли заголовок окна отображать заголовок документа взятый из элемента Title словаря информации о документе.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Флаг, указывающий, должен ли заголовок окна отображать заголовок документа, взятый из элемента Title словаря информации о документе.

```csharp
public bool DisplayDocTitle { get; set; }
```

### Примечания

Если`ЛОЖЬ`, вместо этого в строке заголовка должно отображаться имя файла PDF, содержащего документ.

Этот флаг требуется для соответствия PDF/UA.`истинный` значение будет использоваться автоматически при сохранении в PDF/UA.

Значение по умолчанию`ЛОЖЬ`.

### Примеры

Показывает, как отобразить заголовок документа в виде строки заголовка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
// Установите «DisplayDocTitle» в «true», чтобы получить некоторые программы для чтения PDF, такие как Adobe Acrobat Pro,
// для отображения значения встроенного свойства документа "Заголовок" на вкладке, принадлежащей этому документу.
// Установите «DisplayDocTitle» в «false», чтобы такие программы чтения отображали имя файла документа.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


