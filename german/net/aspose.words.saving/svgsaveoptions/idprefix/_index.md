---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „SvgSaveOptions IdPrefix“, die Element-IDs in Ihrem Ausgabedokument für bessere Organisation und Übersichtlichkeit anpasst. Optimieren Sie Ihre SVG-Dateien noch heute!
type: docs
weight: 40
url: /de/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

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

Zeigt, wie ein Präfix hinzugefügt wird, das allen generierten Element-IDs (SVG) vorangestellt wird.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### Siehe auch

* class [SvgSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
