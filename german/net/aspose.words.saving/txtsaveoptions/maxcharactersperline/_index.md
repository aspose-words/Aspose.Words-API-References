---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words für .NET
description: Entdecken Sie TxtSaveOptions MaxCharactersPerLine und legen Sie ganz einfach Zeichenbegrenzungen pro Zeile für eine bessere Textformatierung fest. Der Standardwert ist 0 für unbegrenzte Zeichen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Ruft einen ganzzahligen Wert ab oder legt ihn fest, der die maximale Anzahl von Zeichen pro Zeile angibt. Der Standardwert ist 0, d. h. keine Begrenzung.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Beispiele

Zeigt, wie die maximale Anzahl von Zeichen pro Zeile festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Legen Sie 30 Zeichen als maximal zulässige Zahl pro Zeile fest.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Siehe auch

* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
