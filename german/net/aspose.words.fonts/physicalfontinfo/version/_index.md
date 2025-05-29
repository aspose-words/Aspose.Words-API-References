---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words für .NET
description: Entdecken Sie die Versionseigenschaft „PhysicalFontInfo“ und greifen Sie einfach auf die Versionszeichenfolge der Schriftart zu, um die Designkonsistenz und die Typografie zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

Versionszeichenfolge der Schriftart.

```csharp
public string Version { get; }
```

## Beispiele

Zeigt, wie verfügbare Schriftarten aufgelistet werden.

```csharp
// Konfigurieren Sie Aspose.Words so, dass Schriftarten aus einem benutzerdefinierten Ordner bezogen werden, und drucken Sie dann alle verfügbaren Schriftarten.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Siehe auch

* class [PhysicalFontInfo](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
