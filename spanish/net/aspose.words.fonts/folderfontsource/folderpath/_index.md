---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: Aspose.Words para .NET
description: Descubre la propiedad FolderFontSource FolderPath para acceder fácilmente a tu carpeta de fuentes. ¡Optimiza tu flujo de trabajo de diseño hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Ruta a la carpeta.

```csharp
public string FolderPath { get; }
```

## Ejemplos

Muestra cómo utilizar una carpeta de sistema local que contiene fuentes como fuente de fuentes.

```csharp
// Crea una fuente de fuente desde una carpeta que contiene archivos de fuente.
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

* class [FolderFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
