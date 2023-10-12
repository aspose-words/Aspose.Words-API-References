---
title: Class AsposeWordsPrintDocument
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Rendering.AsposeWordsPrintDocument klass. Ger en standardimplementering för utskrift av enDocument inom .NETutskriftsramverket.
type: docs
weight: 4530
url: /sv/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Ger en standardimplementering för utskrift av en[`Document`](../../aspose.words/document/) inom .NET-utskriftsramverket.

För att lära dig mer, besök[Skriva ut ett dokument programmerat eller använda dialogrutor](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) dokumentationsartikel.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(Document) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Hämtar eller ställer in hur icke-färgade sidor skrivs ut om enheten stöder färgutskrift. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Får antalet sidor som skrivs ut i färg (dvs. medColor satt till sant). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Läser och cachar vissa fält avPrinterSettings för att minska utskriftstiden. |

### Anmärkningar

`AsposeWordsPrintDocument` åsidosätterPrintEventArgs) för att skriva ut det intervall av sidor som anges iPrinterSettings.

Ett enda Word-dokument kan bestå av flera sektioner som anger sidor med olika storlekar, orientering och pappersfack.`AsposeWordsPrintDocument` åsidosätter QueryPageSettingsEventArgs) för att korrekt välja pappersstorlek, orientering och papperskälla när du skriver ut ett Word-dokument.

Microsoft Word lagrar skrivarspecifika värden för pappersfack i ett Word-dokument och därför kommer endast utskrift på samma skrivarmodell som den som valdes när användaren angav pappersfack att resultera i utskrift från rätt fack. Om du skriver ut ett dokument på en annan skrivare, kommer troligen standardpappersfacket att användas, inte de fack som anges i dokumentet.

### Se även

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)


