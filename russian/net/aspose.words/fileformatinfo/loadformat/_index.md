---
title: FileFormatInfo.LoadFormat
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatInfo свойство. Получает обнаруженный формат документа.
type: docs
weight: 40
url: /ru/net/aspose.words/fileformatinfo/loadformat/
---
## FileFormatInfo.LoadFormat property

Получает обнаруженный формат документа.

```csharp
public LoadFormat LoadFormat { get; }
```

### Примечания

Когда документ OOXML зашифрован, невозможно определить, является ли он документом Excel, Word или PowerPoint, не расшифровав его предварительно, поэтому для зашифрованного документа OOXML это свойство всегда будет возвращать значение.Docx.

### Примеры

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../fileformatinfo/)
* сборка [Aspose.Words](../../../)


