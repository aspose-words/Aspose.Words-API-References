---
title: OoxmlSaveOptions.Password
second_title: Aspose.Words per .NET API Reference
description: OoxmlSaveOptions proprietà. Ottiene/imposta una password per crittografare il documento utilizzando lalgoritmo di crittografia standard ECMA376.
type: docs
weight: 50
url: /it/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Ottiene/imposta una password per crittografare il documento utilizzando l'algoritmo di crittografia standard ECMA376.

```csharp
public string Password { get; set; }
```

### Osservazioni

Per salvare il documento senza crittografia, questa proprietà dovrebbe essere`nullo` o stringa vuota.

### Esempi

Mostra come creare un documento Office Open XML crittografato con password.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Non saremo in grado di aprire questo documento con Microsoft Word o
// Aspose.Words senza fornire la password corretta.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Apre il documento crittografato passando la password corretta in un oggetto LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


