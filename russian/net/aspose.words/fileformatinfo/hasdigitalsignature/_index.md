---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FileFormatInfo HasDigitalSignature — быстро проверьте, содержит ли ваш документ цифровую подпись, что повышает безопасность и подлинность.
type: docs
weight: 20
url: /ru/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Возврат`истинный`если этот документ содержит цифровую подпись. Это свойство просто информирует о наличии цифровой подписи в документе, , но не указывает, действительна ли подпись или нет.

```csharp
public bool HasDigitalSignature { get; }
```

## Примечания

Это свойство существует, чтобы помочь вам отсортировать документы с цифровой подписью от документов без нее. Если вы используете Aspose.Words для изменения и сохранения документа с цифровой подписью, то цифровая подпись будет утеряна. Это сделано намеренно, поскольку цифровая подпись существует для защиты подлинности документа. Используя это свойство, вы можете обнаружить документы с цифровой подписью перед их обработкой так же, как и обычные документы, и предпринять некоторые действия, чтобы избежать потери цифровой подписи, например, уведомить пользователя.

## Примеры

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

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
