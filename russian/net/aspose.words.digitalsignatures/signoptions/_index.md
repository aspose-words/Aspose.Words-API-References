---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DigitalSignatures.SignOptions, чтобы настроить процесс подписания документов с помощью гибких и безопасных параметров для улучшения рабочего процесса.
type: docs
weight: 620
url: /ru/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Позволяет указать параметры подписания документа.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public class SignOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [SignOptions](signoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Указывает комментарии к цифровой подписи. Значение по умолчанию:**пустая строка**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | Пароль для расшифровки исходного документа. Значение по умолчанию:**пустая строка** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | Указывает идентификатор класса поставщика подписи. Значение по умолчанию:**Пусто (все нули) Guid** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | Идентификатор строки подписи. Значение по умолчанию:**Пусто (все нули) Guid** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | Изображение, которое будет показано в связанном[`SignatureLine`](../../aspose.words.drawing/signatureline/) . Значение по умолчанию:`нулевой` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | Дата подписания. Значение по умолчанию:**текущее время** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | Указывает уровень цифровой подписи на основе стандарта XML-DSig. Значение по умолчанию:XmlDSig . |

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

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
