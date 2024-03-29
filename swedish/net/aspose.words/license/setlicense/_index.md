---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words för .NET
description: License SetLicense metod. Licensierar komponenten i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Licensierar komponenten.

```csharp
public void SetLicense(string licenseName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| licenseName | String | Kan vara ett fullständigt eller kort filnamn eller namn på en inbäddad resurs. Använd en tom sträng för att växla till utvärderingsläge. |

## Anmärkningar

Försöker hitta licensen på följande platser:

1. Explicit väg.

2. Mappen som innehåller Aspose-komponentsammansättningen.

3. Mappen som innehåller klientens anropssammansättning.

4. Mappen som innehåller posten (start) assembly.

5. En inbäddad resurs i klientens anropssammansättning.

**Notera:**På .NET Compact Framework försöker du hitta licensen endast på dessa platser:

1. Explicit väg.

2. En inbäddad resurs i klientens anropssammansättning.

## Exempel

Visar hur man initierar en licens för Aspose.Words med hjälp av en licensfil i det lokala filsystemet.

```csharp
// Ställ in licensen för vår Aspose.Words-produkt genom att skicka det lokala filsystemets filnamn för en giltig licensfil.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Skapa en kopia av vår licensfil i mappen binärer i vår applikation.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Om vi skickar ett filnamn utan en sökväg,
// SetLicense kommer att söka på flera lokala filsystemplatser för denna fil.
// En av dessa platser kommer att vara mappen "bin", som innehåller en kopia av vår licensfil.
license.SetLicense("Aspose.Words.NET.lic");
```

### Se även

* class [License](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## SetLicense(*Stream*) {#setlicense}

Licensierar komponenten.

```csharp
public void SetLicense(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | En stream som innehåller licensen. |

## Anmärkningar

Använd den här metoden för att ladda en licens från en stream.

## Exempel

Visar hur man initierar en licens för Aspose.Words från en ström.

```csharp
// Ställ in licensen för vår Aspose.Words-produkt genom att skicka en ström för en giltig licensfil i vårt lokala filsystem.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Se även

* class [License](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
