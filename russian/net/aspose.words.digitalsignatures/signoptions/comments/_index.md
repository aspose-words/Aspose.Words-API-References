---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SignOptions Comments, чтобы улучшить вашу цифровую подпись с помощью пользовательских заметок. Улучшите ясность и коммуникацию без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

Указывает комментарии к цифровой подписи. Значение по умолчанию:**пустая строка**(Empty ).

```csharp
public string Comments { get; set; }
```

## Примеры

Показывает, как подписывать документы цифровой подписью.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создайте комментарий и дату, которые будут применены к нашей новой цифровой подписи.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Берем неподписанный документ из локальной файловой системы через файловый поток,
// затем создаем его подписанную копию, определяемую именем файла выходного потока.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Смотрите также

* class [SignOptions](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
