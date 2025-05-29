---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.CompressionLevel для оптимизации размеров файлов OOXML, повышения производительности и эффективности обработки документов.
type: docs
weight: 5610
url: /ru/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Уровень сжатия для файлов OOXML.

(Файлы DOCX и DOTX по сути являются ZIP-архивом, это свойство управляет уровнем сжатия архива.

Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому данное свойство не влияет на файлы FlatOpc.)

```csharp
public enum CompressionLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Нормальный уровень сжатия. Уровень сжатия по умолчанию, используемый Aspose.Words. |
| Maximum | `1` | Максимальный уровень сжатия. |
| Fast | `2` | Уровень быстрого сжатия. |
| SuperFast | `3` | Уровень сверхбыстрого сжатия. Microsoft Word использует этот уровень сжатия. |

## Примеры

Показывает, как указать уровень сжатия, используемый при сохранении документа OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передаем его в метод сохранения документа, чтобы изменить способ сохранения документа.
// Установите свойство "CompressionLevel" на "CompressionLevel.Maximum", чтобы применить самое сильное и самое медленное сжатие.
// Установите свойство "CompressionLevel" на "CompressionLevel.Normal" для применения
// сжатие по умолчанию, которое Aspose.Words использует при сохранении документов OOXML.
// Установите свойство "CompressionLevel" на "CompressionLevel.Fast", чтобы применить более быстрое и слабое сжатие.
// Установите свойство "CompressionLevel" на "CompressionLevel.SuperFast" для применения
// сжатие по умолчанию, используемое Microsoft Word.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
