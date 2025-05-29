---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words för .NET
description: Ta enkelt bort bindestrecksordböcker för alla språk med UnregisterDictionary-metoden, vilket förbättrar textens tydlighet och läsbarhet.
type: docs
weight: 50
url: /sv/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Avregistrerar en bindestreckslexikon för det angivna språket.

Detta skiljer sig från att registrera en null-ordbok. Att avregistrera en ordbok möjliggör återanrop för det angivna språket.

```csharp
public static void UnregisterDictionary(string language)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| language | String | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "kulturnamn" och RFC 4646 för mer information. |

## Exempel

Visar hur man registrerar en bindestreckslexikon.

```csharp
// En bindestreckslexikon innehåller en lista med strängar som definierar bindestrecksregler för ordbokens språk.
// När ett dokument innehåller textrader där ett ord kan delas upp och fortsätta på nästa rad,
// bindestreck söker igenom ordbokens lista med strängar efter det ordets delsträngar.
// Om ordboken innehåller en delsträng, så kommer bindestreck att dela ordet över två rader
// av delsträngen och lägg till ett bindestreck i den första halvan.
// Registrera en ordboksfil från det lokala filsystemet till språkinställningen "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med en språkinställning som matchar vår ordlista,
// och spara det i ett fast sidformat. Texten i det dokumentet kommer att vara avstreckad.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ladda om dokumentet efter att ordboken avregistrerats,
// och spara den i en annan PDF-fil, som inte kommer att ha bindestreckstext.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Se även

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
