---
title: Hyphenation.IsDictionaryRegistered
second_title: Aspose.Words per .NET API Reference
description: Hyphenation metodo. Restituiscefalso se per la lingua specificata non è registrato alcun dizionario o se è registrato un dizionario nulloVERO altrimenti.
type: docs
weight: 30
url: /it/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Restituisce`falso` se per la lingua specificata non è registrato alcun dizionario o se è registrato un dizionario nullo,`VERO` altrimenti.

```csharp
public static bool IsDictionaryRegistered(string language)
```

### Esempi

Mostra come registrare un dizionario di sillabazione.

```csharp
// Un dizionario di sillabazione contiene un elenco di stringhe che definiscono le regole di sillabazione per la lingua del dizionario.
// Quando un documento contiene righe di testo in cui una parola può essere divisa e continuata nella riga successiva,
// la sillabazione cercherà nell'elenco di stringhe del dizionario le sottostringhe di quella parola.
// Se il dizionario contiene una sottostringa, la sillabazione dividerà la parola su due righe
// dalla sottostringa e aggiunge un trattino alla prima metà.
// Registra un file dizionario dal file system locale alla locale "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Apre un documento contenente testo con una lingua corrispondente a quella del nostro dizionario,
// e salvarlo in un formato di salvataggio a pagina fissa. Il testo in quel documento sarà sillabato.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Ricarica il documento dopo aver annullato la registrazione del dizionario,
// e salvarlo in un altro PDF, che non avrà testo sillabato.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Guarda anche

* class [Hyphenation](../)
* spazio dei nomi [Aspose.Words](../../hyphenation/)
* assemblea [Aspose.Words](../../../)


