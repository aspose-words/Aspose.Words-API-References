---
title: Sign
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 30
url: /net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil.Sign method (1 of 4)

Signs source document using given [`CertificateHolder`](../../certificateholder) and [`SignOptions`](../../signoptions) with digital signature and writes signed document to destination stream.

Document should be either Doc or Docx.

**Output will be written to the start of stream and stream size will be updated with content length.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | Stream | The stream which contains the document to sign. |
| dstStream | Stream | The stream that signed document will be written to. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) object with various signing options. |

## Examples

Shows how to digitally sign documents.

```csharp
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Create a comment and date which will be applied with our new digital signature.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### See Also

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* assembly [Aspose.Words](../../../)

---

## DigitalSignatureUtil.Sign method (2 of 4)

Signs source document using given [`CertificateHolder`](../../certificateholder) and [`SignOptions`](../../signoptions) with digital signature and writes signed document to destination file.

Document should be either Doc or Docx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | String | The file name of the document to sign. |
| dstFileName | String | The file name of the signed document output. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) object with various signing options. |

## Examples

Shows how to add a signature line to a document, and then sign it using a digital certificate.

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
        /// Creates a copy of a source document signed using provided signee information and X509 certificate.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Configure and insert a signature line, an object in the document that will display a signature that we sign it with.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // First, we will save an unsigned version of our document.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Overwrite the unsigned document we saved above with a version signed using the certificate.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Converts an image to a byte array.
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

### See Also

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* assembly [Aspose.Words](../../../)

---

## DigitalSignatureUtil.Sign method (3 of 4)

Signs source document using given [`CertificateHolder`](../../certificateholder) with digital signature and writes signed document to destination stream.

Document should be either Doc or Docx.

**Output will be written to the start of stream and stream size will be updated with content length.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | Stream | The stream which contains the document to sign. |
| dstStream | Stream | The stream that signed document will be written to. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## Examples

Shows how to sign documents with X.509 certificates.

```csharp
// Verify that a document is not signed.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Take a document from a stream and save a signed copy to another stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Please verify that all of the document's digital signatures are valid and check their details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### See Also

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* assembly [Aspose.Words](../../../)

---

## DigitalSignatureUtil.Sign method (4 of 4)

Signs source document using given [`CertificateHolder`](../../certificateholder) with digital signature and writes signed document to destination file.

Document should be either Doc or Docx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | String | The file name of the document to sign. |
| dstFileName | String | The file name of the signed document output. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## Examples

Shows how to sign documents with X.509 certificates.

```csharp
// Verify that a document is not signed.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Take a document from a stream and save a signed copy to another stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Please verify that all of the document's digital signatures are valid and check their details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### See Also

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* namespace [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
