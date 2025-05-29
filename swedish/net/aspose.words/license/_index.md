---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words för .NET
description: Frigör Aspose.Words fulla potential med vår licensklass. Hantera enkelt licensiering för sömlös dokumenthantering och förbättrad funktionalitet.
type: docs
weight: 3870
url: /sv/net/aspose.words/license/
---
## License class

Tillhandahåller metoder för att licensiera komponenten.

För att lära dig mer, besök[Licensiering och prenumeration](https://docs.aspose.com/words/net/licensing/) dokumentationsartikel.

```csharp
public class License
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [License](license/)() | Initierar en ny instans av den här klassen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Licensierar komponenten. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Licensierar komponenten. |

## Exempel

Visar hur man initierar en licens för Aspose.Words med hjälp av en licensfil i det lokala filsystemet.

```csharp
// Ställ in licensen för vår Aspose.Words-produkt genom att skicka det lokala filsystemsfilnamnet för en giltig licensfil.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Skapa en kopia av vår licensfil i binärmappen i vår applikation.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Om vi skickar ett filnamn utan sökväg,
// SetLicense kommer att söka efter den här filen i flera lokala filsystem.
// En av dessa platser kommer att vara "bin"-mappen, som innehåller en kopia av vår licensfil.
license.SetLicense("Aspose.Words.NET.lic");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
