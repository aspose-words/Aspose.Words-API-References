---
title: Sign
second_title: Справочник по API Aspose.Words для .NET
description: Подписывает исходный документ используя данныеCertificateHolderaspose.words.digitalsignatures/certificateholder а такжеSignOptionsaspose.words.digitalsignatures/signoptions с цифровой подписью и записывает подписанный документ в поток назначения.
type: docs
weight: 30
url: /ru/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Подписывает исходный документ, используя данные[`CertificateHolder`](../../certificateholder) а также[`SignOptions`](../../signoptions) с цифровой подписью и записывает подписанный документ в поток назначения.

Документ должен быть либоDoc или жеDocx.

**Вывод будет записан в начало потока, а размер потока будет обновляться в зависимости от длины содержимого.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcStream | Stream | Поток, содержащий документ для подписи. |
| dstStream | Stream | Поток, в который будет записан подписанный документ. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) объект с сертификатом, который использовался для подписи файла. Сертификат в держателе ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) объект с различными вариантами подписи. |

### Примеры

Показывает, как подписывать документы цифровой подписью.

```csharp
// Создайте сертификат X.509 из хранилища PKCS#12, который должен содержать закрытый ключ.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Создайте комментарий и дату, которые будут применяться с нашей новой цифровой подписью.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Берём неподписанный документ из локальной файловой системы через файловый поток,
// затем создайте его подписанную копию, определяемую именем файла выходного файлового потока.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Смотрите также

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* сборка [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Подписывает исходный документ, используя данные[`CertificateHolder`](../../certificateholder) а также[`SignOptions`](../../signoptions) с цифровой подписью и записывает подписанный документ в файл назначения.

Документ должен быть либоDoc или жеDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcFileName | String | Имя файла документа для подписи. |
| dstFileName | String | Имя файла вывода подписанного документа. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) объект с сертификатом, который использовался для подписи файла. Сертификат в держателе ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) объект с различными вариантами подписи. |

### Примеры

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```csharp
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
        /// Создает копию исходного документа, подписанную с использованием предоставленной информации о подписывающей стороне и сертификата X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Настраиваем и вставляем строку подписи, объект в документе, который будет отображать подпись, которой мы его подписываем.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Во-первых, мы сохраним неподписанную версию нашего документа.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Перезаписать неподписанный документ, который мы сохранили выше, версией, подписанной с использованием сертификата.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Преобразует изображение в массив байтов.
        /// </summary>
        private static byte[] ImageToByteArray(Image imageIn)
        {
            using (MemoryStream ms = new MemoryStream())
            {
                imageIn.Save(ms, ImageFormat.Png);
                return ms.ToArray();
            }
        }
#endif

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
            mSignees = new List<Signee>
            {
                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg"))),
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes),
                #endif

                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg")))
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes)
                #endif
            };
        }

        private static List<Signee> mSignees;
```

### Смотрите также

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* сборка [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Подписывает исходный документ, используя данные[`CertificateHolder`](../../certificateholder)с цифровой подписью и записывает подписанный документ в поток назначения.

Документ должен быть либоDoc или жеDocx.

**Вывод будет записан в начало потока, а размер потока будет обновляться в зависимости от длины содержимого.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcStream | Stream | Поток, содержащий документ для подписи. |
| dstStream | Stream | Поток, в который будет записан подписанный документ. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) объект с сертификатом, который использовался для подписи файла. Сертификат в держателе ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable. |

### Примеры

Показывает, как подписывать документы сертификатами X.509.

```csharp
// Проверяем, что документ не подписан.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Создадим объект CertificateHolder из файла PKCS12, который мы будем использовать для подписи документа.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Есть два способа сохранить подписанную копию документа в локальную файловую систему:
// 1 - Назначить документ именем локального системного файла и сохранить подписанную копию в месте, указанном другим именем файла.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Взять документ из потока и сохранить подписанную копию в другой поток.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Убедитесь, что все цифровые подписи документа действительны, и проверьте их данные.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Смотрите также

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* сборка [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Подписывает исходный документ, используя данные[`CertificateHolder`](../../certificateholder) с цифровой подписью и записывает подписанный документ в файл назначения.

Документ должен быть либоDoc или жеDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcFileName | String | Имя файла документа для подписи. |
| dstFileName | String | Имя файла вывода подписанного документа. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) объект с сертификатом, который использовался для подписи файла. Сертификат в держателе ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable. |

### Примеры

Показывает, как подписывать документы сертификатами X.509.

```csharp
// Проверяем, что документ не подписан.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Создадим объект CertificateHolder из файла PKCS12, который мы будем использовать для подписи документа.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Есть два способа сохранить подписанную копию документа в локальную файловую систему:
// 1 - Назначить документ именем локального системного файла и сохранить подписанную копию в месте, указанном другим именем файла.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Взять документ из потока и сохранить подписанную копию в другой поток.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Убедитесь, что все цифровые подписи документа действительны, и проверьте их данные.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Смотрите также

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* пространство имен [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
