---
title: HyphenationOptions.AutoHyphenation
second_title: Aspose.Words für .NET-API-Referenz
description: HyphenationOptions eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft istFALSCH .
type: docs
weight: 20
url: /de/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob die automatische Silbentrennung für das Dokument aktiviert ist. Der Standardwert für diese Eigenschaft ist`FALSCH` .

```csharp
public bool AutoHyphenation { get; set; }
```

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


