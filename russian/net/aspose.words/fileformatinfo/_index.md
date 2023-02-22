---
title: Class FileFormatInfo
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.FileFormatInfo сорт. Содержит данные возвращенныеFileFormatUtil методы определения формата документа.
type: docs
weight: 2630
url: /ru/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Содержит данные, возвращенные[`FileFormatUtil`](../fileformatutil/) методы определения формата документа.

```csharp
public class FileFormatInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Получает обнаруженную кодировку, если она применима к текущему формату документа. На данный момент определяет кодировку только для документов HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Возвращает true, если этот документ содержит цифровую подпись. Это свойство просто информирует о наличии цифровой подписи в документе, , но не указывает, является ли подпись действительной или нет. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Возвращает значение true, если документ зашифрован и для его открытия требуется пароль. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Получает обнаруженный формат документа. |

### Примечания

Вы не создаете экземпляры этого класса напрямую. Объекты этого класса возвращаются [`DetectFileFormat`](../fileformatutil/detectfileformat/)методы.

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


