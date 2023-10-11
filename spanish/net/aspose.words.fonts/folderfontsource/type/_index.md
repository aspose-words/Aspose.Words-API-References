---
title: FolderFontSource.Type
second_title: Referencia de API de Aspose.Words para .NET
description: FolderFontSource propiedad. Devuelve el tipo de fuente fuente.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Devuelve el tipo de fuente fuente.

```csharp
public override FontSourceType Type { get; }
```

### Ejemplos

Muestra cómo utilizar una carpeta del sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ver también

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../folderfontsource/)
* asamblea [Aspose.Words](../../../)


