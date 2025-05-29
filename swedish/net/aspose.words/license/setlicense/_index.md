---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words för .NET
description: Licensiera dina komponenter enkelt med vår SetLicense-metod. Lås upp all funktionalitet och förbättra ditt projekts potential idag!
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
| licenseName | String | Kan vara ett fullständigt eller kort filnamn eller namnet på en inbäddad resurs. Använd en tom sträng för att växla till utvärderingsläge. |

## Anmärkningar

Försöker hitta licensen på följande platser:

1. Explicit sökväg.

2. Mappen som innehåller Aspose-komponentsammansättningen.

3. Mappen som innehåller klientens anropande sammansättning.

4. Mappen som innehåller postens (startup) sammansättning.

5. En inbäddad resurs i klientens anropande sammansättning.

**Notera:**Försöker bara hitta licensen på dessa platser i .NET Compact Framework:

1. Explicit sökväg.

2. En inbäddad resurs i klientens anropande sammansättning.

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

---

## SetLicense(*Stream*) {#setlicense}

Licensierar komponenten.

```csharp
public void SetLicense(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | En ström som innehåller licensen. |

## Anmärkningar

Använd den här metoden för att läsa in en licens från en ström.

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
