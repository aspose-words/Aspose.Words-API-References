---
title: HyphenationOptions.ConsecutiveHyphenLimit
second_title: Aspose.Words für .NET-API-Referenz
description: HyphenationOptions eigendom. Ruft die maximale Anzahl aufeinanderfolgender Zeilen ab die mit Bindestrichen enden können oder legt diese fest. Der Standardwert für diese Eigenschaft ist 0.
type: docs
weight: 30
url: /de/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

Ruft die maximale Anzahl aufeinanderfolgender Zeilen ab, die mit Bindestrichen enden können, oder legt diese fest. Der Standardwert für diese Eigenschaft ist 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

### Bemerkungen

Wenn der Wert dieser Eigenschaft auf 0 gesetzt ist, können beliebig viele aufeinanderfolgende Zeilen mit Bindestrichen enden.

Die Eigenschaft hat keine Auswirkung beim Speichern in festen Seitenformaten, z. B. PDF.

### Beispiele

Zeigt, wie die automatische Silbentrennung konfiguriert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Siehe auch

* class [HyphenationOptions](../)
* namensraum [Aspose.Words.Settings](../../hyphenationoptions/)
* Montage [Aspose.Words](../../../)


