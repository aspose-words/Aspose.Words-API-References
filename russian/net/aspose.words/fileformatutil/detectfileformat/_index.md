---
title: FileFormatUtil.DetectFileFormat
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatUtil метод. Обнаруживает и возвращает информацию о формате документа хранящегося в файле на диске.
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

А[`FileFormatInfo`](../../fileformatinfo/) объект, содержащий обнаруженную информацию.

### Примечания

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ действителен. Этот метод определяет формат документа только путем считывания данных, достаточных для обнаружения. Чтобы полностью убедиться, что документ действителен , вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выдает[`FileCorruptedException`](../../filecorruptedexception/) когда формат распознан, но обнаружение не может быть завершено из-за повреждения.

### Примеры

Показывает, как использовать класс FileFormatUtil для определения формата и шифрования документа.

```csharp
Document doc = new Document();

// Настроить объект SaveOptions для шифрования документа
// с паролем, когда мы его сохраняем, а затем сохраняем документ.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Проверяем тип файла нашего документа и его статус шифрования.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
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

А[`FileFormatInfo`](../../fileformatinfo/) объект, содержащий обнаруженную информацию.

### Примечания

Поток должен располагаться в начале документа.

Когда этот метод возвращается, положение в потоке восстанавливается до исходного положения.

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ действителен. Этот метод определяет формат документа только путем считывания данных, достаточных для обнаружения. Чтобы полностью убедиться, что документ действителен , вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выдает[`FileCorruptedException`](../../filecorruptedexception/) когда формат распознан, но обнаружение не может быть завершено из-за повреждения.

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
    // 1 — Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Преобразование LoadFormat напрямую в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока, а затем сохраните его в файле с автоматически обнаруженным расширением.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
* сборка [Aspose.Words](../../../)


