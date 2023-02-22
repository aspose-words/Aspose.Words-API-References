---
title: HyphenationOptions.HyphenateCaps
second_title: Aspose.Words für .NET-API-Referenz
description: HyphenationOptions eigendom. Erhält oder legt einen Wert fest der bestimmt ob Wörter die ausschließlich in Großbuchstaben geschrieben sind getrennt werden. Der Standardwert für diese Eigenschaft ist Stimmt .
type: docs
weight: 40
url: /de/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Erhält oder legt einen Wert fest, der bestimmt, ob Wörter, die ausschließlich in Großbuchstaben geschrieben sind, getrennt werden. Der Standardwert für diese Eigenschaft ist **Stimmt** .

```csharp
public bool HyphenateCaps { get; set; }
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


