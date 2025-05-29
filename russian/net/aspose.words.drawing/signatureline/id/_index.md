---
title: SignatureLine.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SignatureLine Id, чтобы легко управлять идентификаторами строки подписи и настраивать их для бесшовной интеграции документов и улучшения пользовательского опыта.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/signatureline/id/
---
## SignatureLine.Id property

Получает или задает идентификатор для этой строки подписи.

Этот идентификатор может быть связан с цифровой подписью при подписании документа с использованием[`DigitalSignatureUtil`](../../../aspose.words.digitalsignatures/digitalsignatureutil/). Это значение должно быть уникальным и по умолчанию оно генерируется случайным образом new Guid (NewGuid).

```csharp
public Guid Id { get; set; }
```

## Примеры

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

* class [SignatureLine](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
