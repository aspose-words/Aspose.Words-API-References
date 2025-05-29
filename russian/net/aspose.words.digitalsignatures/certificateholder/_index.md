---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.DigitalSignatures.CertificateHolder — ваш ключ к управлению экземплярами X509Certificate2 для безопасных цифровых подписей.
type: docs
weight: 570
url: /ru/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Представляет держателя**X509Сертификат2** экземпляр.

Чтобы узнать больше, посетите[Работа с цифровыми подписями](https://docs.aspose.com/words/net/working-with-digital-signatures/) документальная статья.

```csharp
public class CertificateHolder
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Возвращает экземпляр**X509Сертификат2** который содержит закрытые, открытые ключи и цепочку сертификатов. |

## Методы

| Имя | Описание |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | Создает`CertificateHolder` объект, использующий байтовый массив хранилища PKCS12 и его пароль. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | Создает`CertificateHolder` объект, использующий байтовый массив хранилища PKCS12 и его пароль. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | Создает`CertificateHolder`объект, использующий путь к хранилищу PKCS12 и его пароль. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | Создает`CertificateHolder` объект, использующий путь к хранилищу PKCS12, его пароль и псевдоним, с помощью которого будут найдены закрытый ключ и сертификат. |

## Примечания

`CertificateHolder` может быть создан только статическими фабричными методами. Он содержит экземпляр**X509Сертификат2** который используется для введения в систему закрытых, открытых ключей и цепочек сертификатов. Этот класс применяется в[`DigitalSignatureUtil`](../digitalsignatureutil/) и[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) вместо устаревших методов с X509Certificate2 как параметры.

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

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```csharp
[Description("WORDSNET-16868")]
public static void Sign()
{
    string signeeName = "Ron Williams";
    string srcDocumentPath = MyDir + "Document.docx";
    string dstDocumentPath = ArtifactsDir + "SignDocumentCustom.Sign.docx";
    string certificatePath = MyDir + "morzal.pfx";
    string certificatePassword = "aw";

    CreateSignees();

    Signee signeeInfo = mSignees.Find(c => c.Name == signeeName);

    if (signeeInfo != null)
        SignDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
    else
        Assert.Fail("Signee does not exist.");
}

/// <summary>
/// Создает копию исходного документа, подписанного с использованием предоставленной информации о подписавшей стороне и сертификата X509.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Настраиваем и вставляем строку подписи — объект в документе, который будет отображать подпись, которой мы его подписываем.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // Сначала мы сохраним неподписанную версию нашего документа.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Перезаписываем неподписанный документ, который мы сохранили выше, версией, подписанной с использованием сертификата.
    DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

public class Signee
{
    public Guid PersonId { get; set; }
    public string Name { get; set; }
    public string Position { get; set; }
    public byte[] Image { get; set; }

    public Signee(Guid guid, string name, string position, byte[] image)
    {
        PersonId = guid;
        Name = name;
        Position = position;
        Image = image;
    }
}

private static void CreateSignees()
{
    var signImagePath = ImageDir + "Logo.jpg";

    mSignees = new List<Signee>
    {
        new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", TestUtil.ImageToByteArray(signImagePath)),
        new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", TestUtil.ImageToByteArray(signImagePath))
    };
}

private static List<Signee> mSignees;
```

### Смотрите также

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
