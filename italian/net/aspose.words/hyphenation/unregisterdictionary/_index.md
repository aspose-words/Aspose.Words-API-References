---
title: UnregisterDictionary
second_title: Aspose.Words per .NET API Reference
description: Annulla la registrazione di un dizionario di sillabazione per la lingua specificata.
type: docs
weight: 50
url: /it/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Annulla la registrazione di un dizionario di sillabazione per la lingua specificata.

È diverso dalla registrazione del dizionario Null. L'annullamento della registrazione di un dizionario abilita la richiamata per la lingua specificata.

```csharp
public static void UnregisterDictionary(string language)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Vedere la documentazione .NET per "nome cultura" e RFC 4646 per i dettagli. |

### Esempi

Mostra come registrare un dizionario di sillabazione.

```csharp
// Un dizionario di sillabazione contiene un elenco di stringhe che definiscono le regole di sillabazione per la lingua del dizionario.
// Quando un documento contiene righe di testo in cui una parola può essere suddivisa e continuata nella riga successiva,
// la sillabazione cercherà nell'elenco di stringhe del dizionario le sottostringhe di quella parola.
// Se il dizionario contiene una sottostringa, la sillabazione dividerà la parola su due righe
// dalla sottostringa e aggiungi un trattino alla prima metà.
// Registra un file dizionario dal file system locale nella locale "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apri un documento contenente del testo con una localizzazione corrispondente a quella del nostro dizionario,
// e salvalo in un formato di salvataggio a pagina fissa. Il testo in quel documento sarà sillabato.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ricarica il documento dopo aver annullato la registrazione del dizionario,
// e salvalo in un altro PDF, che non avrà testo con sillabazione.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Guarda anche

* class [Hyphenation](../../hyphenation)
* spazio dei nomi [Aspose.Words](../../hyphenation)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
