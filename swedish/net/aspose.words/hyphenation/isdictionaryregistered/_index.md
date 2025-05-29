---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words för .NET
description: Upptäck metoden Hyphenation IsDictionaryRegistered, som kontrollerar om en ordbok är registrerad för ditt språk och säkerställer korrekt bindestreck i dina applikationer.
type: docs
weight: 30
url: /sv/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Returer`falsk` om det inte finns någon registrerad ordbok för det angivna språket, eller om det är en nullordbok registrerad,`sann` annars.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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
