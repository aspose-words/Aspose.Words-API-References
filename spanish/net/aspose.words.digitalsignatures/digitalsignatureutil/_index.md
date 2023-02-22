---
title: Class DigitalSignatureUtil
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.DigitalSignatures.DigitalSignatureUtil clase. Proporciona métodos para firmar documentos.
type: docs
weight: 400
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Proporciona métodos para firmar documentos.

```csharp
public static class DigitalSignatureUtil
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(Stream) | Carga firmas digitales del documento usando stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(string) | Carga firmas digitales del documento. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(Stream, Stream) | Elimina todas las firmas digitales del documento en el flujo de origen y escribe el documento sin firmar en el flujo de destino. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(string, string) | Elimina todas las firmas digitales del archivo de origen y escribe el archivo sin firmar en el archivo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(Stream, Stream, CertificateHolder) | Firma el documento de origen usando dado[`CertificateHolder`](../certificateholder/)con firma digital y escribe el documento firmado en el flujo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(string, string, CertificateHolder) | Firma el documento de origen usando dado[`CertificateHolder`](../certificateholder/) con firma digital y escribe el documento firmado en el archivo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(Stream, Stream, CertificateHolder, SignOptions) | Firma el documento de origen usando dado[`CertificateHolder`](../certificateholder/) y[`SignOptions`](../signoptions/) con firma digital y escribe el documento firmado en el flujo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(string, string, CertificateHolder, SignOptions) | Firma el documento de origen usando dado[`CertificateHolder`](../certificateholder/) y[`SignOptions`](../signoptions/) con firma digital y escribe el documento firmado en el archivo de destino. |

### Observaciones

Dado que la firma digital funciona con el contenido del archivo en lugar del modelo de objeto del documento, estos métodos se colocan en una clase separada.

Los formatos admitidos sonDoc yDocx.

### Ejemplos

Muestra cómo cargar firmas desde un documento firmado digitalmente.

```csharp
// Hay dos formas de cargar la colección de firmas digitales de un documento firmado utilizando la clase DigitalSignatureUtil.
// 1 - Cargar desde un documento desde un sistema de archivos local nombre de archivo:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Si esta colección no está vacía, entonces podemos verificar que el documento está firmado digitalmente.
Assert.AreEqual(1, digitalSignatures.Count);

// 2 - Cargar desde un documento desde un FileStream:
using (Stream stream = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    digitalSignatures = DigitalSignatureUtil.LoadSignatures(stream);
    Assert.AreEqual(1, digitalSignatures.Count);
}
```

Muestra cómo eliminar firmas digitales de un documento firmado digitalmente.

```csharp
// Hay dos formas de usar la clase DigitalSignatureUtil para eliminar firmas digitales
// de un documento firmado guardando una copia sin firmar en otro lugar del sistema de archivos local.
// 1 - Determine las ubicaciones tanto del documento firmado como de la copia sin firmar mediante cadenas de nombre de archivo:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determinar las ubicaciones tanto del documento firmado como de la copia sin firmar por secuencias de archivos:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifique que nuestros dos documentos de salida no tengan firmas digitales.
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx"), Is.Empty);
Assert.That(DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx"), Is.Empty);
```

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../)


