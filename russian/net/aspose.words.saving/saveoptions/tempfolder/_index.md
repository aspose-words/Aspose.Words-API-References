---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words для .NET
description: SaveOptions TempFolder свойство. Указывает папку для временных файлов используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значениенулевой и никакие временные файлы не используются на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение`нулевой` и никакие временные файлы не используются.

```csharp
public string TempFolder { get; set; }
```

## Примечания

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию, эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока сохраняется документ. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, , то скачок памяти во время сохранения может быть достаточно значительным, чтобы заставить систему выдать ошибку.OutOfMemoryException . Указание временной папки с помощью`TempFolder` заставит Aspose.Words хранить внутренние структуры во временных файлах вместо памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступна для записи, в противном случае будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

## Примеры

Показывает, как использовать жесткий диск вместо памяти при сохранении документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Когда мы сохраняем документ, различные элементы временно сохраняются в памяти во время операции сохранения.
// Мы можем использовать эту опцию, чтобы вместо этого использовать временную папку в локальной файловой системе,
// что уменьшит нагрузку на память нашего приложения.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Указанная временная папка должна существовать в локальной файловой системе до операции сохранения.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Папка сохранится без остаточного содержимого после операции загрузки.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
