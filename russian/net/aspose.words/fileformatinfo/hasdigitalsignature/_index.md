---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words для .NET
description: FileFormatInfo HasDigitalSignature свойство. Возвращаетистинныйесли этот документ содержит цифровую подпись. Это свойство просто сообщает что в документе присутствует цифровая подпись  но не указывает действительна ли подпись или нет на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Возвращает`истинный`если этот документ содержит цифровую подпись. Это свойство просто сообщает, что в документе присутствует цифровая подпись, , но не указывает, действительна ли подпись или нет.

```csharp
public bool HasDigitalSignature { get; }
```

## Примечания

Это свойство существует, чтобы помочь вам сортировать документы, имеющие цифровую подпись, от тех, которые не имеют цифровой подписи. Если вы используете Aspose.Words для изменения и сохранения документа, имеющего цифровую подпись, цифровая подпись будет потеряна. Это сделано специально, поскольку существует цифровая подпись для защиты подлинности документа. Используя это свойство, вы можете обнаружить документы с цифровой подписью перед их обработкой так же, как и обычные документы , и предпринять некоторые действия, чтобы избежать потери цифровой подписи, например уведомить пользователя.

## Примеры

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

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
