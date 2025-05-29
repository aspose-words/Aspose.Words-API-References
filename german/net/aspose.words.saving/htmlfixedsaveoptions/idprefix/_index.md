---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words für .NET
description: Entdecken Sie die HtmlFixedSaveOptions IdPrefix-Eigenschaft, um Element-IDs in Ihren Dokumenten anzupassen. Verbessern Sie die Organisation mit maßgeschneiderten Präfixen für eine bessere Ausgabe!
type: docs
weight: 100
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

Gibt ein Präfix an, das allen generierten Element-IDs im Ausgabedokument vorangestellt wird. Der Standardwert ist null und es wird kein Präfix vorangestellt.

```csharp
public string IdPrefix { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Der Wert erfüllt nicht die oben genannten Anforderungen. |

## Bemerkungen

Wenn das Präfix angegeben ist, darf es nur Buchstaben, Ziffern, Unterstriche und Bindestriche enthalten, und muss mit einem Buchstaben beginnen.

## Beispiele

Zeigt, wie ein Präfix hinzugefügt wird, das allen generierten Element-IDs vorangestellt wird.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
