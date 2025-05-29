---
title: DigitalSignatureUtil Class
linktitle: DigitalSignatureUtil
articleTitle: DigitalSignatureUtil
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.DigitalSignatures.DigitalSignatureUtil para firmar documentos fácilmente con firmas digitales seguras. ¡Mejore la integridad de sus documentos hoy mismo!
type: docs
weight: 610
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class

Proporciona métodos para firmar documentos.

Para obtener más información, visite el[Trabajar con firmas digitales](https://docs.aspose.com/words/net/working-with-digital-signatures/) Artículo de documentación.

```csharp
public static class DigitalSignatureUtil
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures)(*Stream*) | Carga firmas digitales del documento mediante stream. |
| static [LoadSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/#loadsignatures_1)(*string*) | Carga firmas digitales del documento. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures)(*Stream, Stream*) | Elimina todas las firmas digitales del documento en el flujo de origen y escribe el documento sin firmar en el flujo de destino. |
| static [RemoveAllSignatures](../../aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/#removeallsignatures_1)(*string, string*) | Elimina todas las firmas digitales del archivo de origen y escribe el archivo sin firmar en el archivo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign)(*Stream, Stream, [CertificateHolder](../certificateholder/)*) | Firma el documento fuente usando lo indicado[`CertificateHolder`](../certificateholder/) con firma digital y escribe el documento firmado en el flujo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_2)(*string, string, [CertificateHolder](../certificateholder/)*) | Firma el documento fuente usando lo indicado[`CertificateHolder`](../certificateholder/) con firma digital y escribe el documento firmado en el archivo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_1)(*Stream, Stream, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Firma el documento fuente usando lo indicado[`CertificateHolder`](../certificateholder/) y[`SignOptions`](../signoptions/) con firma digital y escribe documento firmado en el flujo de destino. |
| static [Sign](../../aspose.words.digitalsignatures/digitalsignatureutil/sign/#sign_3)(*string, string, [CertificateHolder](../certificateholder/), [SignOptions](../signoptions/)*) | Firma el documento fuente usando lo indicado[`CertificateHolder`](../certificateholder/) y[`SignOptions`](../signoptions/) con firma digital y escribe documento firmado en archivo de destino. |

## Observaciones

Dado que la firma digital funciona con el contenido del archivo en lugar del modelo de objetos del documento, estos métodos se colocan en una clase separada.

Los formatos admitidos son: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

## Ejemplos

Muestra cómo cargar firmas desde un documento firmado digitalmente.

```csharp
// Hay dos formas de cargar la colección de firmas digitales de un documento firmado utilizando la clase DigitalSignatureUtil.
// 1 - Cargar desde un documento desde un sistema de archivos local nombre de archivo:
DigitalSignatureCollection digitalSignatures = 
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

// Si esta colección no está vacía, podemos verificar que el documento esté firmado digitalmente.
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
// Hay dos formas de utilizar la clase DigitalSignatureUtil para eliminar firmas digitales
// de un documento firmado guardando una copia sin firmar del mismo en otro lugar del sistema de archivos local.
// 1 - Determine las ubicaciones tanto del documento firmado como de la copia sin firmar mediante cadenas de nombre de archivo:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determinar las ubicaciones tanto del documento firmado como de la copia no firmada mediante flujos de archivos:
using (Stream streamIn = new FileStream(MyDir + "Digitally signed.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx", FileMode.Create))
    {
        DigitalSignatureUtil.RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verifique que nuestros dos documentos de salida no tengan firmas digitales.
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").Count);
Assert.AreEqual(0, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").Count);
```

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../)
