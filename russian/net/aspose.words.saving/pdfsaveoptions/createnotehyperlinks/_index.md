---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words для .NET
description: Улучшите свои PDF-файлы с помощью CreateNoteHyperlinks в PdfSaveOptions. Преобразуйте сноски и концевые сноски в кликабельные ссылки для легкой навигации. По умолчанию — false.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Указывает, следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте статьи в активные гиперссылки. При щелчке по гиперссылке будет открыта соответствующая сноска/концевая сноска. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Примеры

Показывает, как сделать так, чтобы обычные и концевые сноски функционировали как гиперссылки.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "CreateNoteHyperlinks" в значение "true", чтобы включить все символы сносок/концевых сносок
// в тексте действуют как ссылки, при нажатии на которые мы переходим к соответствующим сноскам/концевым примечаниям.
// Установите свойство "CreateNoteHyperlinks" в значение "false", чтобы символы сносок/концевых сносок не ссылались ни на что.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
