---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words per .NET
description: Rimuovi senza sforzo i dizionari di sillabazione per qualsiasi lingua con il metodo UnregisterDictionary, migliorando la chiarezza e la leggibilità del testo.
type: docs
weight: 50
url: /it/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Annulla la registrazione di un dizionario di sillabazione per la lingua specificata.

Questo è diverso dalla registrazione di un dizionario Null. Annullare la registrazione di un dizionario abilita il callback per la lingua specificata.

```csharp
public static void UnregisterDictionary(string language)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| language | String | Un nome di lingua, ad esempio "en-US". Per i dettagli, vedere la documentazione .NET per il "nome della cultura" e RFC 4646. |

## Esempi

Mostra come registrare un dizionario di sillabazione.

```csharp
// Un dizionario di sillabazione contiene un elenco di stringhe che definiscono le regole di sillabazione per la lingua del dizionario.
// Quando un documento contiene righe di testo in cui una parola potrebbe essere suddivisa e continuata sulla riga successiva,
// la sillabazione cercherà le sottostringhe di quella parola nell'elenco delle stringhe del dizionario.
// Se il dizionario contiene una sottostringa, la sillabazione dividerà la parola su due righe
// dalla sottostringa e aggiungi un trattino alla prima metà.
// Registra un file di dizionario dal file system locale alle impostazioni locali "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apri un documento contenente testo con impostazioni locali corrispondenti a quelle del nostro dizionario,
// e salvarlo in un formato di salvataggio a pagina fissa. Il testo in quel documento verrà sillabato.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ricarica il documento dopo aver annullato la registrazione del dizionario,
// e salvarlo in un altro PDF, che non avrà testo con trattino.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Guarda anche

* class [Hyphenation](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
