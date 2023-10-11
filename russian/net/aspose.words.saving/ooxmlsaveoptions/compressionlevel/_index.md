---
title: OoxmlSaveOptions.CompressionLevel
second_title: Справочник по API Aspose.Words для .NET
description: OoxmlSaveOptions свойство. Указывает уровень сжатия используемый для сохранения документа. Значение по умолчаниюNormal .
type: docs
weight: 30
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Указывает уровень сжатия, используемый для сохранения документа. Значение по умолчанию:Normal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### Примеры

Показывает, как указать уровень сжатия, который будет использоваться при сохранении документа OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передаем его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите для свойства CompressionLevel значение CompressionLevel.Maximum, чтобы применить самое сильное и самое медленное сжатие.
// Установите для свойства CompressionLevel значение CompressionLevel.Normal, чтобы применить его.
// сжатие по умолчанию, которое Aspose.Words использует при сохранении документов OOXML.
// Установите для свойства CompressionLevel значение CompressionLevel.Fast, чтобы применить более быстрое и более слабое сжатие.
// Установите для свойства CompressionLevel значение CompressionLevel.SuperFast, чтобы применить его.
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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* сборка [Aspose.Words](../../../)


