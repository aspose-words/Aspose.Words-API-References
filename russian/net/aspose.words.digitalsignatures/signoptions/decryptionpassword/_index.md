---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words для .NET
description: Разблокируйте свои документы без усилий с помощью функции DecryptionPassword от SignOptions. Безопасно расшифруйте исходные файлы с легкостью; по умолчанию — пустая строка.
type: docs
weight: 30
url: /ru/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

Пароль для расшифровки исходного документа. Значение по умолчанию:**пустая строка** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## Примечания

Если документ OOXML зашифрован, необходимо указать пароль дешифрования для расшифровки исходного документа перед его подписанием. Это не требуется для документов в двоичном формате DOC.

## Примеры

Показывает, как подписать зашифрованный файл документа.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создайте комментарий, дату и пароль для расшифровки, которые будут применяться с нашей новой цифровой подписью.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Задайте имя локального системного файла для неподписанного входного документа и имя выходного файла для его новой копии с цифровой подписью.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Смотрите также

* class [SignOptions](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
