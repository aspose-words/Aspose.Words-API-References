---
title: "SignatureLine"
linktitle: "SignatureLine"
second_title: "Aspose.Words para Java"
description: "Proporciona acceso a las propiedades de la línea de firma en Java."
type: docs
weight: 621
url: /es/java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

Proporciona acceso a las propiedades de la línea de firma.

Para obtener más información, visite el artículo de documentación [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getAllowComments()](#getAllowComments) | Obtiene un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo de firma. |
| [getDefaultInstructions()](#getDefaultInstructions) | Obtiene un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign. |
| [getEmail()](#getEmail) | Obtiene la dirección de correo electrónico sugerida del firmante. |
| [getId()](#getId) | Obtiene el identificador de esta línea de firma. |
| [getInstructions()](#getInstructions) | Obtiene las instrucciones para el firmante que se muestran al firmar la línea de firma. |
| [getProviderId()](#getProviderId) | Obtiene el identificador del proveedor de firma para esta línea de firma. |
| [getShowDate()](#getShowDate) | Obtiene un valor que indica que la fecha de firma se muestra en la línea de firma. |
| [getSigner()](#getSigner) | Obtiene el firmante sugerido de la línea de firma. |
| [getSignerTitle()](#getSignerTitle) | Obtiene el título sugerido del firmante (por ejemplo, Gerente). |
| [isSigned()](#isSigned) | Indica que la línea de firma está firmada con una firma digital. |
| [isValid()](#isValid) | Indica que la línea de firma está firmada con una firma digital y que dicha firma digital es válida. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | Establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Sign. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | Establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign. |
| [setEmail(String value)](#setEmail-java.lang.String) | Establece la dirección de correo electrónico sugerida del firmante. |
| [setId(UUID value)](#setId-java.util.UUID) | Establece el identificador para esta línea de firma. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | Establece las instrucciones para el firmante que se muestran al firmar la línea de firma. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Establece el identificador del proveedor de firma para esta línea de firma. |
| [setShowDate(boolean value)](#setShowDate-boolean) | Establece un valor que indica que la fecha de firma se muestra en la línea de firma. |
| [setSigner(String value)](#setSigner-java.lang.String) | Establece el firmante sugerido de la línea de firma. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Establece el título sugerido del firmante (por ejemplo, Gerente). |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


Obtiene un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es false.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
boolean - Un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Sign.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


Obtiene un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign. El valor predeterminado para esta propiedad es true.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
boolean - Un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Sign.
### getEmail() {#getEmail}
```
public String getEmail()
```


Obtiene la dirección de correo electrónico sugerida del firmante. El valor predeterminado para esta propiedad es **empty string**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
java.lang.String - Dirección de correo electrónico sugerida del firmante.
### getId() {#getId}
```
public UUID getId()
```


Obtiene el identificador de esta línea de firma.

Este identificador puede asociarse con una firma digital, al firmar el documento usando [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). Este valor debe ser único y, por defecto, se genera aleatoriamente un nuevo Guid.

 **Examples:** 

Muestra cómo agregar una línea de firma a un documento y luego firmarlo usando un certificado digital.

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
java.util.UUID - Identificador de esta línea de firma.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


Obtiene las instrucciones para el firmante que se muestran al firmar la línea de firma. Esta propiedad se ignora si se establece [getDefaultInstructions()](../../com.aspose.words/signatureline/\\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\\#setDefaultInstructions-boolean). El valor predeterminado para esta propiedad es **cadena vacía**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
java.lang.String - Instrucciones para el firmante que se muestran al firmar la línea de firma.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Obtiene el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es \"{00000000-0000-0000-0000-000000000000}\".

 **Remarks:** 

El proveedor de servicios criptográficos (CSP) es un módulo de software independiente que realmente ejecuta algoritmos criptográficos para autenticación, codificación y cifrado. MS Office reserva el valor de \\{00000000-0000-0000-0000-000000000000\\} para su proveedor de firma predeterminado.

El GUID del proveedor adicionalmente instalado debe obtenerse de la documentación suministrada con el proveedor.

Además, todos los proveedores criptográficos instalados se enumeran en el registro de Windows. Se puede encontrar en la siguiente ruta: HKLM\\\\SOFTWARE\\\\Microsoft\\\\Cryptography\\\\Defaults\\\\Provider. Existe una clave llamada \"CP Service UUID\" que corresponde a un GUID del proveedor de firma.

 **Examples:** 

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

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
java.util.UUID - Identificador del proveedor de firma para esta línea de firma.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


Obtiene un valor que indica que la fecha de firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es true.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
boolean - Un valor que indica que la fecha de firma se muestra en la línea de firma.
### getSigner() {#getSigner}
```
public String getSigner()
```


Obtiene el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es **empty string**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
java.lang.String - Firmante sugerido de la línea de firma.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Obtiene el título sugerido del firmante (por ejemplo, Gerente). El valor predeterminado para esta propiedad es **cadena vacía**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
java.lang.String - Título sugerido del firmante (por ejemplo, Gerente).
### isSigned() {#isSigned}
```
public boolean isSigned()
```


Indica que la línea de firma está firmada con una firma digital.

 **Examples:** 

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

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
boolean - El valor  boolean  correspondiente.
### isValid() {#isValid}
```
public boolean isValid()
```


Indica que la línea de firma está firmada con una firma digital y que dicha firma digital es válida.

 **Examples:** 

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

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
boolean - El valor  boolean  correspondiente.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


Establece un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es  false .

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica que el firmante puede agregar comentarios en el cuadro de diálogo Firmar. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Establece un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Firmar. El valor predeterminado para esta propiedad es  true .

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica que las instrucciones predeterminadas se muestran en el cuadro de diálogo Firmar. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Establece la dirección de correo electrónico sugerida del firmante. El valor predeterminado para esta propiedad es **empty string**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Dirección de correo electrónico sugerida del firmante. |

### setId(UUID value) {#setId-java.util.UUID}
```
public void setId(UUID value)
```


Establece el identificador para esta línea de firma.

Este identificador puede asociarse con una firma digital, al firmar el documento usando [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). Este valor debe ser único y, por defecto, se genera aleatoriamente un nuevo Guid.

 **Examples:** 

Muestra cómo agregar una línea de firma a un documento y luego firmarlo usando un certificado digital.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.UUID | Identificador de esta línea de firma. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


Establece las instrucciones para el firmante que se muestran al firmar la línea de firma. Esta propiedad se ignora si se establece [getDefaultInstructions()](../../com.aspose.words/signatureline/\\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\\#setDefaultInstructions-boolean). El valor predeterminado para esta propiedad es **cadena vacía**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Instrucciones para el firmante que se muestran al firmar la línea de firma. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Establece el identificador del proveedor de firma para esta línea de firma. El valor predeterminado es \"{00000000-0000-0000-0000-000000000000}\".

 **Remarks:** 

El proveedor de servicios criptográficos (CSP) es un módulo de software independiente que realmente ejecuta algoritmos criptográficos para autenticación, codificación y cifrado. MS Office reserva el valor de \\{00000000-0000-0000-0000-000000000000\\} para su proveedor de firma predeterminado.

El GUID del proveedor adicionalmente instalado debe obtenerse de la documentación suministrada con el proveedor.

Además, todos los proveedores criptográficos instalados se enumeran en el registro de Windows. Se puede encontrar en la siguiente ruta: HKLM\\\\SOFTWARE\\\\Microsoft\\\\Cryptography\\\\Defaults\\\\Provider. Existe una clave llamada \"CP Service UUID\" que corresponde a un GUID del proveedor de firma.

 **Examples:** 

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.UUID | Identificador del proveedor de firma para esta línea de firma. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


Establece un valor que indica que la fecha de firma se muestra en la línea de firma. El valor predeterminado para esta propiedad es  true .

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica que la fecha de firma se muestra en la línea de firma. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


Establece el firmante sugerido de la línea de firma. El valor predeterminado para esta propiedad es **empty string**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Firmante sugerido de la línea de firma. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Establece el título sugerido del firmante (por ejemplo, Gerente). El valor predeterminado para esta propiedad es **cadena vacía**.

 **Examples:** 

Muestra cómo crear una línea para una firma e insertarla en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Título sugerido del firmante (por ejemplo, Gerente). |

