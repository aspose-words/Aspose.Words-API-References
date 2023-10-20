---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: FolderFontSource Type proprietà. Restituisce il tipo di fonte del carattere in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Restituisce il tipo di fonte del carattere.

```csharp
public override FontSourceType Type { get; }
```

## Esempi

Mostra come utilizzare una cartella di sistema locale che contiene i caratteri come origine dei caratteri.

```csharp
// Crea un'origine carattere da una cartella che contiene file di caratteri.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Guarda anche

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
