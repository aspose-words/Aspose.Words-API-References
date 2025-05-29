---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad FolderFontSourceType. Identifique fácilmente los tipos de fuentes para optimizar sus proyectos de diseño y su flujo de trabajo.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Devuelve el tipo de la fuente de origen.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
