---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words för .NET
description: HtmlSaveOptions NavigationMapLevel fast egendom. Anger den maximala nivån för rubriker som fylls på i navigationskartan vid export till formaten EPUB MOBI eller AZW3 . Standardvärdet är3  i C#.
type: docs
weight: 390
url: /sv/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Anger den maximala nivån för rubriker som fylls på i navigationskartan vid export till formaten EPUB, MOBI eller AZW3 . Standardvärdet är`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Anmärkningar

Navigationskartan tillåter användaragenter att tillhandahålla ett enkelt sätt att navigera genom dokumentstrukturen. Vanligtvis motsvarar navigeringspunkterna rubriker i dokumentet. För att fylla rubriker upp till nivå**N** tilldela detta värde till`NavigationMapLevel`.

Som standard är tre nivåer av rubriker ifyllda: stycken med stilar**Rubrik 1** ,**Rubrik 2** och**Rubrik 3**. Du kan ställa in den här egenskapen till ett värde från 1 till 9 för att begära motsvarande maxnivå. Om du ställer in den på noll kommer navigationskartan att reduceras till endast dokumentets rot eller rötter för dokumentdelar.

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
