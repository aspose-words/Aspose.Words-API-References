---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words для .NET
description: FileFormatUtil DetectFileFormat метод. Обнаруживает и возвращает информацию о формате документа хранящегося в дисковом файле на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Обнаруживает и возвращает информацию о формате документа, хранящегося в дисковом файле.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла. |

### Возвращаемое значение

А[`FileFormatInfo`](../../fileformatinfo/) объект, содержащий обнаруженную информацию.

## Примечания

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ действителен. Этот метод определяет формат документа только путем чтения данных, достаточных для обнаружения. Чтобы полностью убедиться в том, что документ действителен, вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выбрасывает[`FileCorruptedException`](../../filecorruptedexception/) когда формат распознан, но обнаружение не может быть завершено из-за повреждения.

## Примеры

Показывает, как использовать класс FileFormatUtil для определения формата и шифрования документа.

```csharp
Document doc = new Document();

// Настраиваем объект SaveOptions для шифрования документа
// с паролем, когда мы его сохраняем, а затем сохраняем документ.
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

Поток должен располагаться в начале документа.

Когда этот метод завершает работу, позиция в потоке восстанавливается в исходное положение.

Даже если этот метод определяет формат документа, он не гарантирует , что указанный документ действителен. Этот метод определяет формат документа только путем чтения данных, достаточных для обнаружения. Чтобы полностью убедиться в том, что документ действителен, вам необходимо загрузить документ в[`Document`](../../document/) объект.

Этот метод выбрасывает[`FileCorruptedException`](../../filecorruptedexception/) когда формат распознан, но обнаружение не может быть завершено из-за повреждения.

## Примеры

Показывает, как использовать методы FileFormatUtil для определения формата документа.

```csharp
// Загрузите документ из файла, у которого отсутствует расширение файла, а затем определите его формат файла.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Ниже приведены два метода преобразования LoadFormat в соответствующий SaveFormat.
    // 1 — Получить строку расширения файла для LoadFormat, затем получить соответствующий SaveFormat из этой строки:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 — преобразовать LoadFormat непосредственно в его SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока, а затем сохраните его с автоматически определенным расширением файла.
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
