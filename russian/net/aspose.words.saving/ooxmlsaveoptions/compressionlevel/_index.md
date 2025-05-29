---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OoxmlSaveOptions CompressionLevel, чтобы оптимизировать сохранение документов с помощью настраиваемых уровней сжатия для повышения производительности.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Указывает уровень сжатия, используемый для сохранения документа. Значение по умолчанию:Normal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
