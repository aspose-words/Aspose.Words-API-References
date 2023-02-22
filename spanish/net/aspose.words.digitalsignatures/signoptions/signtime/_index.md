---
title: SignOptions.SignTime
second_title: Referencia de API de Aspose.Words para .NET
description: SignOptions propiedad. La fecha de la firma. El valor predeterminado es tiempo actual Now .
type: docs
weight: 70
url: /es/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

La fecha de la firma. El valor predeterminado es **tiempo actual** (Now ).

```csharp
public DateTime SignTime { get; set; }
```

### Ejemplos

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Cree un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego cree una copia firmada determinada por el nombre de archivo de la secuencia del archivo de salida.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ver también

* class [SignOptions](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../signoptions/)
* asamblea [Aspose.Words](../../../)


