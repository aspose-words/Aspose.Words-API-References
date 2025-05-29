---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words per .NET
description: Proteggi i tuoi documenti con OoxmlSaveOptions! Imposta facilmente una password per la crittografia utilizzando lo standard ECMA376 per una maggiore protezione dei dati.
type: docs
weight: 60
url: /it/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

Ottiene/imposta una password per crittografare il documento utilizzando l'algoritmo di crittografia standard ECMA376.

```csharp
public string Password { get; set; }
```

## Osservazioni

Per salvare il documento senza crittografia questa proprietà dovrebbe essere`null` o stringa vuota.

## Esempi

Mostra come creare un documento Office Open XML crittografato tramite password.

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

// Aprire il documento crittografato passando la password corretta in un oggetto LoadOptions.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
