---
title: DetectFileFormat
second_title: Справочник по API Aspose.Words для .NET
description: Обнаруживает и возвращает информацию о формате документа хранящегося в файле на диске.
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(string) {#detectfileformat_1}

Обнаруживает и возвращает информацию о формате документа, хранящегося в файле на диске.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла. |

### Возвращаемое значение

A[`FileFormatInfo`](../../fileformatinfo)объект, содержащий обнаруженную информацию.

### Примечания

Даже если этот метод определяет формат документа, он не гарантирует указанный документ действителен. Этот метод определяет формат документа только путем чтения данных, достаточных для обнаружения. Чтобы полностью убедиться, что документ действителен вам необходимо загрузить документ в объект[`Document`](../../document).

Этот метод выдает[`FileCorruptedException`](../../filecorruptedexception)когда формат распознан, но обнаружение не может быть завершено из-за коррупции.

### Примеры

Показывает, как использовать класс FileFormatUtil для определения формата и шифрования документа.

```csharp
 // Используйте экземпляр FileFormatInfo, чтобы убедиться, что документ не имеет цифровой подписи.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

 // Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Мы можем загрузить и получить доступ к подписям подписанного документа в такой коллекции.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

Показывает, как использовать класс FileFormatUtil для определения формата документа и наличия цифровых подписей.

```csharp
 // Используйте экземпляр FileFormatInfo, чтобы убедиться, что документ не имеет цифровой подписи.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

 // Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Мы можем загрузить и получить доступ к подписям подписанного документа в такой коллекции.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Смотрите также

* class [FileFormatInfo](../../fileformatinfo)
* class [FileFormatUtil](../../fileformatutil)
* пространство имен [Aspose.Words](../../fileformatutil)
* сборка [Aspose.Words](../../../)

---

## DetectFileFormat(Stream) {#detectfileformat}

Обнаруживает и возвращает информацию о формате документа, хранящегося в потоке.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток. |

### Возвращаемое значение

A[`FileFormatInfo`](../../fileformatinfo)объект, содержащий обнаруженную информацию.

### Примечания

Поток должен располагаться в начале документа.

Когда этот метод возвращается, позиция в потоке восстанавливается до исходной позиции.

Даже если этот метод определяет формат документа, он не гарантирует что указанный документ действителен. Этот метод определяет формат документа только путем чтения данных, достаточных для обнаружения. Чтобы полностью убедиться, что документ действителен вам необходимо загрузить документ в объект[`Document`](../../document).

Этот метод выдает[`FileCorruptedException`](../../filecorruptedexception)когда формат распознан, но обнаружение не может быть завершено из-за коррупции.

### Примеры

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
 // Загрузить документ из файла, в котором отсутствует расширение файла, а затем определить его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

     // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
     // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки: 
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

     // 2 - Конвертировать LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

     // Загружаем документ из потока, а затем сохраняем его в файл с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* class [FileFormatInfo](../../fileformatinfo)
* class [FileFormatUtil](../../fileformatutil)
* пространство имен [Aspose.Words](../../fileformatutil)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
