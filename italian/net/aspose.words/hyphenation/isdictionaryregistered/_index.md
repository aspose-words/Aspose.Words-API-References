---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words per .NET
description: Scopri il metodo Hyphenation IsDictionaryRegistered, controlla se un dizionario è registrato per la tua lingua, assicurando una sillabazione accurata nelle tue applicazioni.
type: docs
weight: 30
url: /it/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Restituisce`falso` se per la lingua specificata non è registrato alcun dizionario o se registrato è un dizionario Null,`VERO` altrimenti.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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
