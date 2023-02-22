---
title: Hyphenation.IsDictionaryRegistered
second_title: Aspose.Words för .NET API Referens
description: Hyphenation metod. Returnerar False om det inte finns någon ordbok registrerad för det angivna språket eller om den registreras är Nullordbok annars sant.
type: docs
weight: 30
url: /sv/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Returnerar False om det inte finns någon ordbok registrerad för det angivna språket eller om den registreras är Null-ordbok, annars sant.

```csharp
public static bool IsDictionaryRegistered(string language)
```

### Exempel

Visar hur man registrerar en avstavningsordbok.

```csharp
// En avstavningsordbok innehåller en lista med strängar som definierar avstavningsregler för ordbokens språk.
// När ett dokument innehåller textrader där ett ord kan delas upp och fortsätta på nästa rad,
// Avstavning kommer att titta igenom ordbokens lista med strängar för det ordets delsträngar.
// Om ordboken innehåller en delsträng, kommer avstavning att dela ordet över två rader
// av delsträngen och lägg till ett bindestreck till den första halvan.
// Registrera en ordboksfil från det lokala filsystemet till "de-CH"-lokalen.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öppna ett dokument som innehåller text med ett språk som matchar vår ordbok,
// och spara den i ett sparat format med fast sida. Texten i det dokumentet kommer att avstavas.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ladda om dokumentet efter avregistrering av ordboken,
// och spara den till en annan PDF, som inte kommer att ha avstavad text.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Se även

* class [Hyphenation](../)
* namnutrymme [Aspose.Words](../../hyphenation/)
* hopsättning [Aspose.Words](../../../)


