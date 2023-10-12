---
title: PdfSaveOptions.CreateNoteHyperlinks
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Указывает следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте в активные гиперссылки. При нажатии гиперссылка приведет к соответствующей сноске/концевой сноске. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 50
url: /ru/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Указывает, следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте в активные гиперссылки. При нажатии гиперссылка приведет к соответствующей сноске/концевой сноске. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

### Примеры

Показывает, как заставить сноски и концевые сноски функционировать как гиперссылки.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства CreateNoteHyperlinks значение «true», чтобы повернуть все символы сносок/концевых сносок.
// в тексте действуют как ссылки, которые при нажатии ведут к соответствующим сноскам/концевым сноскам.
// Установите для свойства CreateNoteHyperlinks значение «false», чтобы символы сносок/концевых сносок не ссылались ни на что.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


