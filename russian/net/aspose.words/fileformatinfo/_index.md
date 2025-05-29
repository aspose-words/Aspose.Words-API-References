---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.FileFormatInfo для эффективного определения формата документа. Получите доступ к подробным данным для улучшения ваших решений по управлению файлами.
type: docs
weight: 3220
url: /ru/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Содержит данные, возвращаемые[`FileFormatUtil`](../fileformatutil/) методы определения формата документа.

Чтобы узнать больше, посетите[Определить формат файла и проверить совместимость формата](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) документальная статья.

```csharp
public class FileFormatInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент определяет кодировку только для документов HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Возврат`истинный`если этот документ содержит цифровую подпись. Это свойство просто информирует о наличии цифровой подписи в документе, , но не указывает, действительна ли подпись или нет. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Возврат`истинный` если этот документ содержит макросы VBA. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Возврат`истинный` если документ зашифрован и для его открытия требуется пароль. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Получает обнаруженный формат документа. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Объекты этого класса возвращаются by [`DetectFileFormat`](../fileformatutil/detectfileformat/) методы.

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
