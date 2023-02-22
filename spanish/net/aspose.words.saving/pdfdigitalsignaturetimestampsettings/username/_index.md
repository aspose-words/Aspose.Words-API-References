---
title: PdfDigitalSignatureTimestampSettings.UserName
second_title: Referencia de API de Aspose.Words para .NET
description: PdfDigitalSignatureTimestampSettings propiedad. Nombre de usuario del servidor de marca de tiempo.
type: docs
weight: 50
url: /es/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/username/
---
## PdfDigitalSignatureTimestampSettings.UserName property

Nombre de usuario del servidor de marca de tiempo.

```csharp
public string UserName { get; set; }
```

### Observaciones

El valor por defecto es nulo.

### Ejemplos

Muestra cómo firmar digitalmente un documento PDF guardado y colocarle una marca de tiempo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

  // Crear una firma digital y asignarla a nuestro objeto SaveOptions para firmar el documento cuando lo guardemos en PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crear una marca de tiempo verificada por la autoridad de marca de tiempo.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mi contraseña");

// La vida útil predeterminada de la marca de tiempo es de 100 segundos.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Podemos establecer nuestro período de tiempo de espera a través del constructor.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mi contraseña", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", options.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// El método "Guardar" aplicará nuestra firma al documento de salida en este momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Ver también

* class [PdfDigitalSignatureTimestampSettings](../)
* espacio de nombres [Aspose.Words.Saving](../../pdfdigitalsignaturetimestampsettings/)
* asamblea [Aspose.Words](../../../)


