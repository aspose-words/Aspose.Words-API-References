---
title: DigitalSignatureUtil.RemoveAllSignatures
linktitle: RemoveAllSignatures
articleTitle: RemoveAllSignatures
second_title: Aspose.Words para .NET
description: DigitalSignatureUtil RemoveAllSignatures método. Elimina todas las firmas digitales del archivo de origen y escribe el archivo sin firmar en el archivo de destino en C#.
type: docs
weight: 20
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## RemoveAllSignatures(*string, string*) {#removeallsignatures_1}

Elimina todas las firmas digitales del archivo de origen y escribe el archivo sin firmar en el archivo de destino.

Los siguientes formatos son compatibles para la eliminación de firmas digitales: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(string srcFileName, string dstFileName)
```

## Ejemplos

Muestra cómo eliminar firmas digitales de un documento firmado digitalmente.

```csharp
// Hay dos formas de utilizar la clase DigitalSignatureUtil para eliminar firmas digitales
// de un documento firmado guardando una copia sin firmar en algún otro lugar del sistema de archivos local.
// 1 - Determinar las ubicaciones tanto del documento firmado como de la copia sin firmar mediante cadenas de nombre de archivo:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determinar las ubicaciones tanto del documento firmado como de la copia sin firmar mediante flujos de archivos:
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

* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## RemoveAllSignatures(*Stream, Stream*) {#removeallsignatures}

Elimina todas las firmas digitales del documento en la secuencia de origen y escribe el documento sin firmar en la secuencia de destino.

**La salida se escribirá al inicio de la transmisión y el tamaño de la transmisión se actualizará con la longitud del contenido.**

Los siguientes formatos son compatibles para la eliminación de firmas digitales: Doc , Dot , Docx , Dotx , Docm , Odt , Ott.

```csharp
public static void RemoveAllSignatures(Stream srcStream, Stream dstStream)
```

## Ejemplos

Muestra cómo eliminar firmas digitales de un documento firmado digitalmente.

```csharp
// Hay dos formas de utilizar la clase DigitalSignatureUtil para eliminar firmas digitales
// de un documento firmado guardando una copia sin firmar en algún otro lugar del sistema de archivos local.
// 1 - Determinar las ubicaciones tanto del documento firmado como de la copia sin firmar mediante cadenas de nombre de archivo:
DigitalSignatureUtil.RemoveAllSignatures(MyDir + "Digitally signed.docx",
    ArtifactsDir + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determinar las ubicaciones tanto del documento firmado como de la copia sin firmar mediante flujos de archivos:
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

* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
