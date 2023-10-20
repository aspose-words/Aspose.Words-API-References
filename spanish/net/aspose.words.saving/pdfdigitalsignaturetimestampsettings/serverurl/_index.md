---
title: PdfDigitalSignatureTimestampSettings.ServerUrl
linktitle: ServerUrl
articleTitle: ServerUrl
second_title: Aspose.Words para .NET
description: PdfDigitalSignatureTimestampSettings ServerUrl propiedad. URL del servidor de marca de tiempo en C#.
type: docs
weight: 30
url: /es/net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/serverurl/
---
## PdfDigitalSignatureTimestampSettings.ServerUrl property

URL del servidor de marca de tiempo.

```csharp
public string ServerUrl { get; set; }
```

## Observaciones

El valor predeterminado es`nulo` . Si`nulo` , entonces la firma digital no tendrá marca de tiempo.

## Ejemplos

Muestra cómo firmar digitalmente un documento PDF guardado y ponerle una marca de tiempo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Signed PDF contents.");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Crea una firma digital y asígnala a nuestro objeto SaveOptions para firmar el documento cuando lo guardemos en PDF.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
options.DigitalSignatureDetails = new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", DateTime.Now);

// Crea una marca de tiempo verificada por la autoridad.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MiContraseña");

// La vida útil predeterminada de la marca de tiempo es de 100 segundos.
Assert.AreEqual(100.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);

// Podemos establecer nuestro período de tiempo de espera mediante el constructor.
options.DigitalSignatureDetails.TimestampSettings =
    new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "Mi contraseña", TimeSpan.FromMinutes(30));

Assert.AreEqual(1800.0d, options.DigitalSignatureDetails.TimestampSettings.Timeout.TotalSeconds);
Assert.AreEqual("https://freetsa.org/tsr", opciones.DigitalSignatureDetails.TimestampSettings.ServerUrl);
Assert.AreEqual("JohnDoe", options.DigitalSignatureDetails.TimestampSettings.UserName);
Assert.AreEqual("MyPassword", options.DigitalSignatureDetails.TimestampSettings.Password);

// El método "Guardar" aplicará nuestra firma al documento de salida en este momento.
doc.Save(ArtifactsDir + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

### Ver también

* class [PdfDigitalSignatureTimestampSettings](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
