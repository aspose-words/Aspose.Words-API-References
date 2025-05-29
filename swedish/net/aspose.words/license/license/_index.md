---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words för .NET
description: Skapa och hantera licenser enkelt med vår konstruktorklass. Förenkla din licensieringsprocess och öka effektiviteten idag!
type: docs
weight: 10
url: /sv/net/aspose.words/license/license/
---
## License constructor

Initierar en ny instans av den här klassen.

```csharp
public License()
```

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

* class [License](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
