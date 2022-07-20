---
title: CompressionLevel
second_title: Справочник по API Aspose.Words для .NET
description: Уровень сжатия для файлов OOXML.
type: docs
weight: 4610
url: /ru/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Уровень сжатия для файлов OOXML.

(файлы DOCX и DOTX внутри являются ZIP-архивом, это свойство управляет степенью сжатия архива.

Обратите внимание, что файл FlatOpc не является ZIP-архивом, поэтому это свойство не влияет на файлы FlatOpc.)

```csharp
public enum CompressionLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Нормальный уровень сжатия. Уровень сжатия по умолчанию, используемый Aspose.Words. |
| Maximum | `1` | Максимальный уровень сжатия. |
| Fast | `2` | Уровень быстрого сжатия. |
| SuperFast | `3` | Сверхбыстрый уровень сжатия. Microsoft Word использует этот уровень сжатия. |

### Примеры

Показывает, как указать уровень сжатия для использования при сохранении документа OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// и затем передаем его в метод сохранения документа, чтобы изменить способ сохранения документа.
// Установите для свойства "CompressionLevel" значение "CompressionLevel.Maximum", чтобы применить самое сильное и самое медленное сжатие.
// Установите для свойства "CompressionLevel" значение "CompressionLevel.Normal" для применения
// сжатие по умолчанию, которое Aspose.Words использует при сохранении документов OOXML.
// Установите для свойства "CompressionLevel" значение "CompressionLevel.Fast", чтобы применить более быстрое и слабое сжатие.
// Установите для свойства "CompressionLevel" значение "CompressionLevel.SuperFast" для применения
// сжатие по умолчанию, которое использует Microsoft Word.
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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->