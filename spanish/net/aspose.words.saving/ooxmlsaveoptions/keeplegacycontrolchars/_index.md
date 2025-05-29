---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words para .NET
description: Descubra la propiedad KeepLegacyControlChars de OoxmlSaveOptions para mantener el formato original de los caracteres de control heredados para una conversión de documentos perfecta.
type: docs
weight: 50
url: /es/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Mantiene la representación original de los caracteres de control heredados.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Ejemplos

Muestra cómo admitir caracteres de control heredados al convertir a .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardar del documento para modificar la forma en que guardamos el documento.
// Establezca la propiedad "KeepLegacyControlChars" en "true" para conservar
// el carácter heredado "ShortDateTime" al guardar.
// Establezca la propiedad "KeepLegacyControlChars" en "falso" para eliminar
// el carácter heredado "ShortDateTime" del documento de salida.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Ver también

* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
