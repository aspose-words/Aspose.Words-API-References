---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words для .NET
description: Управляйте своими зашифрованными документами без усилий с помощью свойства LoadOptions Password. Безопасно установите или получите свой пароль для бесперебойного доступа.
type: docs
weight: 110
url: /ru/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

Возвращает или задает пароль для открытия зашифрованного документа. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` .

```csharp
public string Password { get; set; }
```

## Примечания

Вам нужно знать пароль, чтобы открыть зашифрованный документ. Если документ не зашифрован, установите это значение`нулевой` или пустая строка.

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

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
