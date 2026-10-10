---
title: "SignatureLine"
linktitle: "SignatureLine"
second_title: "Aspose.Words для Java"
description: "Предоставляет доступ к свойствам линии подписи в Java."
type: docs
weight: 621
url: /ru/java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

Обеспечивает доступ к свойствам строки подписи.

Чтобы узнать больше, посетите статью документации [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Методы

| Метод | Описание |
| --- | --- |
| [getAllowComments()](#getAllowComments) | Возвращает значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. |
| [getDefaultInstructions()](#getDefaultInstructions) | Получает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign. |
| [getEmail()](#getEmail) | Получает предложенный адрес электронной почты подписанта. |
| [getId()](#getId) | Получает идентификатор этой линии подписи. |
| [getInstructions()](#getInstructions) | Получает инструкции для подписанта, которые отображаются при подписании строки подписи. |
| [getProviderId()](#getProviderId) | Получает идентификатор поставщика подписи для этой линии подписи. |
| [getShowDate()](#getShowDate) | Получает значение, указывающее, что дата подписи отображается в строке подписи. |
| [getSigner()](#getSigner) | Получает предложенного подписанта строки подписи. |
| [getSignerTitle()](#getSignerTitle) | Получает предлагаемое название подписанта (например, Менеджер). |
| [isSigned()](#isSigned) | Указывает, что линия подписи подписана цифровой подписью. |
| [isValid()](#isValid) | Указывает, что линия подписи подписана цифровой подписью и эта цифровая подпись действительна. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | Устанавливает значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | Устанавливает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign. |
| [setEmail(String value)](#setEmail-java.lang.String) | Устанавливает предложенный адрес электронной почты подписанта. |
| [setId(UUID value)](#setId-java.util.UUID) | Устанавливает идентификатор для этой линии подписи. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | Устанавливает инструкции для подписанта, которые отображаются при подписании строки подписи. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Устанавливает идентификатор поставщика подписи для этой линии подписи. |
| [setShowDate(boolean value)](#setShowDate-boolean) | Устанавливает значение, указывающее, что дата подписи отображается в строке подписи. |
| [setSigner(String value)](#setSigner-java.lang.String) | Устанавливает предложенного подписанта строки подписи. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Устанавливает предлагаемое название подписанта (например, Менеджер). |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


Получает значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign.  Значение по умолчанию для этого свойства —  false .

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean — Значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


Получает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign.  Значение по умолчанию для этого свойства —  true .

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean — Значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign.
### getEmail() {#getEmail}
```
public String getEmail()
```


Получает предложенный адрес электронной почты подписанта. Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String — Предложенный адрес электронной почты подписанта.
### getId() {#getId}
```
public UUID getId()
```


Получает идентификатор этой линии подписи.

Этот идентификатор может быть связан с цифровой подписью при подписании документа с помощью [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). Это значение должно быть уникальным, и по умолчанию генерируется случайный новый Guid.

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Returns:**
java.util.UUID - Идентификатор этой строки подписи.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


Получает инструкции для подписанта, которые отображаются при подписании строки подписи. Это свойство игнорируется, если установлен [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean). Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String — Инструкции для подписанта, которые отображаются при подписании строки подписи.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Получает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию — "\{00000000-0000-0000-0000-000000000000\}".

 **Remarks:** 

Криптографический сервисный провайдер (CSP) — независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует значение \{00000000-0000-0000-0000-000000000000\} для своего провайдера подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Их можно найти по следующему пути: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Существует имя ключа "CP Service UUID", которое соответствует GUID провайдера подписи.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Returns:**
java.util.UUID - Идентификатор поставщика подписи для этой строки подписи.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


Получает значение, указывающее, что дата подписи отображается в строке подписи.  Значение по умолчанию для этого свойства —  true .

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean — Значение, указывающее, что дата подписи отображается в строке подписи.
### getSigner() {#getSigner}
```
public String getSigner()
```


Получает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String — Предложенный подписант строки подписи.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Получает предлагаемое должностное наименование подписанта (например, Менеджер). Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String - Предлагаемое должностное наименование подписанта (например, Менеджер).
### isSigned() {#isSigned}
```
public boolean isSigned()
```


Указывает, что линия подписи подписана цифровой подписью.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isValid() {#isValid}
```
public boolean isValid()
```


Указывает, что линия подписи подписана цифровой подписью и эта цифровая подпись действительна.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


Устанавливает значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. Значение по умолчанию для этого свойства — false.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, что подписант может добавлять комментарии в диалоговом окне Sign. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Устанавливает значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign. Значение по умолчанию для этого свойства — true.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, что стандартные инструкции отображаются в диалоговом окне Sign. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Устанавливает предложенный адрес электронной почты подписанта. Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Предложенный адрес электронной почты подписанта. |

### setId(UUID value) {#setId-java.util.UUID}
```
public void setId(UUID value)
```


Устанавливает идентификатор для этой линии подписи.

Этот идентификатор может быть связан с цифровой подписью при подписании документа с помощью [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). Это значение должно быть уникальным, и по умолчанию генерируется случайный новый Guid.

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.UUID | Идентификатор этой строки подписи. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


Устанавливает инструкции для подписанта, которые отображаются при подписании строки подписи. Это свойство игнорируется, если установлен [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean). Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Инструкции для подписанта, которые отображаются при подписании строки подписи. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Устанавливает идентификатор поставщика подписи для этой строки подписи. Значение по умолчанию — "\{00000000-0000-0000-0000-000000000000\}".

 **Remarks:** 

Криптографический сервисный провайдер (CSP) — независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует значение \{00000000-0000-0000-0000-000000000000\} для своего провайдера подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Их можно найти по следующему пути: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Существует имя ключа "CP Service UUID", которое соответствует GUID провайдера подписи.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.UUID | Идентификатор поставщика подписи для этой строки подписи. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


Устанавливает значение, указывающее, что дата подписи отображается в строке подписи. Значение по умолчанию для этого свойства — true.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, что дата подписи отображается в строке подписи. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


Устанавливает предложенного подписанта строки подписи. Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Предложенный подписант строки подписи. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Устанавливает предлагаемое должностное наименование подписанта (например, Менеджер). Значение по умолчанию для этого свойства — **empty string**.

 **Examples:** 

Показывает, как создать линию для подписи и вставить её в документ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Предлагаемое должностное наименование подписанта (например, Менеджер). |

