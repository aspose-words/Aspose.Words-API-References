---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words para .NET
description: OoxmlSaveOptions KeepLegacyControlChars propiedad. Mantiene la representación original de los caracteres de control heredados en C#.
type: docs
weight: 40
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

// Cuando guardamos el documento en formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establece la propiedad "KeepLegacyControlChars" en "true" para preservar
// el carácter heredado "ShortDateTime" mientras se guarda.
// Establece la propiedad "KeepLegacyControlChars" en "false" para eliminar
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
