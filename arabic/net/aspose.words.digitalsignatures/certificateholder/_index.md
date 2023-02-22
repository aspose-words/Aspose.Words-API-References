---
title: Class CertificateHolder
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.DigitalSignatures.CertificateHolder فصل. يمثل صاحب X509 شهادة 2 نموذج.
type: docs
weight: 360
url: /ar/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

يمثل صاحب **X509 شهادة 2** نموذج.

```csharp
public class CertificateHolder
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | إرجاع مثيل **X509 شهادة 2** الذي يحمل المفاتيح الخاصة والعامة وسلسلة الشهادات. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(byte[], SecureString) | إنشاء كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(byte[], string) | إنشاء كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(string, string) | إنشاء كائن CertificateHolder باستخدام المسار إلى مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(string, string, string) | إنشاء كائن CertificateHolder باستخدام المسار إلى مخزن PKCS12 وكلمة المرور والاسم المستعار باستخدام المفتاح الخاص والشهادة التي سيتم العثور عليها. |

### ملاحظات

**حامله الشهاده** يمكن إنشاؤها بواسطة طرق المصنع الثابتة فقط. يحتوي على مثيل **X509 شهادة 2** والذي يستخدم لإدخال المفاتيح الخاصة والعامة وسلاسل الشهادات في النظام. يتم تطبيق هذه الفئة في[`DigitalSignatureUtil`](../digitalsignatureutil/) و[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) بدلاً من الطرق القديمة مع X509Certificate2 كمعلمات.

### أمثلة

يوضح كيفية توقيع ملف المستند المشفر.

```csharp
// أنشئ شهادة X.509 من متجر PKCS # 12 ، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// أنشئ تعليقًا وتاريخًا وكلمة مرور لفك التشفير والتي سيتم تطبيقها مع توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// قم بتعيين اسم ملف نظام محلي لمستند الإدخال غير الموقع ، واسم ملف الإخراج لنسخته الجديدة الموقعة رقمياً.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

يوضح كيفية توقيع المستندات رقميًا.

```csharp
// أنشئ شهادة X.509 من متجر PKCS # 12 ، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// أنشئ تعليقًا وتاريخًا سيتم تطبيقه بتوقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// خذ مستندًا غير موقع من نظام الملفات المحلي عبر تدفق ملف ،
// ثم أنشئ نسخة موقعة منه يحددها اسم ملف تدفق ملف الإخراج.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

يوضح كيفية إضافة سطر توقيع إلى مستند ، ثم توقيعه باستخدام شهادة رقمية.

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
        /// ينشئ نسخة من مستند مصدر موقع باستخدام معلومات الموقّع المقدمة وشهادة X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // تكوين وإدراج سطر توقيع ، وهو كائن في المستند سيعرض توقيعًا نوقعه به.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // أولاً ، سنحفظ نسخة غير موقعة من وثيقتنا.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // اكتب فوق المستند غير الموقع الذي حفظناه أعلاه بإصدار موقع باستخدام الشهادة.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// يحول صورة إلى مصفوفة بايت.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../)


