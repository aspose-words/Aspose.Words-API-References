---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words для .NET
description: Быстро определяйте форматы документов с помощью метода DetectFileFormat от FileFormatUtil. Получайте точные сведения о форматах для эффективного управления файлами.
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Обнаруживает и возвращает информацию о формате документа, хранящегося в файле на диске.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла. |

### Возвращаемое значение

А[`FileFormatInfo`](../../fileformatinfo/) объект, содержащий обнаруженную информацию.

## Примечания

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ является действительным. Этот метод определяет формат документа только , считывая данные, достаточные для определения. Чтобы полностью проверить, что документ является действительным , вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выбрасывает[`FileCorruptedException`](../../filecorruptedexception/) когда формат is распознан, но обнаружение не может быть завершено из-за повреждения.

## Примеры

Показывает, как использовать класс FileFormatUtil для определения формата документа и шифрования.

```csharp
Document doc = new Document();

// Настройте объект SaveOptions для шифрования документа
// с паролем при сохранении, а затем сохраняем документ.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Проверяем тип файла нашего документа и статус его шифрования.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Показывает, как использовать класс FileFormatUtil для определения формата документа и наличия цифровых подписей.

```csharp
// Используйте экземпляр FileFormatInfo, чтобы проверить, что документ не имеет цифровой подписи.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Мы можем загрузить и получить доступ к подписям подписанного документа в такой коллекции.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Смотрите также

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Обнаруживает и возвращает информацию о формате документа, хранящегося в потоке.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток. |

### Возвращаемое значение

А[`FileFormatInfo`](../../fileformatinfo/) объект, содержащий обнаруженную информацию.

## Примечания

Поток должен быть расположен в начале документа.

При возврате этого метода позиция в потоке восстанавливается до исходной позиции.

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ является действительным. Этот метод определяет формат документа только , считывая данные, достаточные для определения. Чтобы полностью проверить, что документ является действительным , вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выбрасывает[`FileCorruptedException`](../../filecorruptedexception/) когда формат is распознан, но обнаружение не может быть завершено из-за повреждения.

## Примеры

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
// Загрузить документ из файла, у которого отсутствует расширение, а затем определить формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Ниже приведены два метода преобразования LoadFormat в соответствующий ему SaveFormat.
    // 1 - Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Преобразовать LoadFormat непосредственно в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загружаем документ из потока, а затем сохраняем его в автоматически обнаруженном расширении файла.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Смотрите также

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
