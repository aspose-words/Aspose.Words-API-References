---
title: DigitalSignatureUtil.LoadSignatures
linktitle: LoadSignatures
articleTitle: LoadSignatures
second_title: Aspose.Words para .NET
description: DigitalSignatureUtil LoadSignatures método. Carga firmas digitales desde el documento en C#.
type: docs
weight: 10
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## LoadSignatures(*string*) {#loadsignatures_1}

Carga firmas digitales desde el documento.

```csharp
public static DigitalSignatureCollection LoadSignatures(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Ruta al documento. |

### Valor_devuelto

Recogida de firmas digitales. Devuelve una colección vacía si el archivo no está firmado.

## Ejemplos

Muestra cómo cargar firmas desde un documento firmado digitalmente.

```csharp
// Hay dos formas de cargar la colección de firmas digitales de un documento firmado utilizando la clase DigitalSignatureUtil.
// 1 - Cargar desde un documento desde un nombre de archivo del sistema de archivos local:
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

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## LoadSignatures(*Stream*) {#loadsignatures}

Carga firmas digitales del documento usando stream.

```csharp
public static DigitalSignatureCollection LoadSignatures(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Transmitir con el documento. |

### Valor_devuelto

Recogida de firmas digitales. Devuelve una colección vacía si el archivo no está firmado.

## Ejemplos

Muestra cómo cargar firmas desde un documento firmado digitalmente.

```csharp
// Hay dos formas de cargar la colección de firmas digitales de un documento firmado utilizando la clase DigitalSignatureUtil.
// 1 - Cargar desde un documento desde un nombre de archivo del sistema de archivos local:
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

### Ver también

* class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
