---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words per .NET
description: Proteggi i tuoi documenti con la proprietà Password di OdtSaveOptions. Imposta o recupera facilmente una password per una crittografia avanzata e una protezione dei dati avanzata.
type: docs
weight: 50
url: /it/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Ottiene o imposta una password per crittografare il documento.

```csharp
public string Password { get; set; }
```

## Osservazioni

Per salvare il documento senza crittografia questa proprietà dovrebbe essere`null` o stringa vuota.

## Esempi

Mostra come crittografare un documento ODT/OTT salvato con una password e quindi caricarlo utilizzando Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un nuovo OdtSaveOptions e passa "SaveFormat.Odt",
 // oppure "SaveFormat.Ott" come formato in cui salvare il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Se apriamo questo documento con un editor appropriato,
// ci verrà richiesta la password specificata nell'oggetto SaveOptions.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Se desideriamo aprire o modificare nuovamente questo documento utilizzando Aspose.Words,
// dovremo fornire un oggetto LoadOptions con la password corretta al costruttore di caricamento.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
