---
title: OdtSaveOptions.Password
second_title: Aspose.Words per .NET API Reference
description: OdtSaveOptions proprietà. Ottiene o imposta una password per crittografare il documento.
type: docs
weight: 40
url: /it/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Ottiene o imposta una password per crittografare il documento.

```csharp
public string Password { get; set; }
```

### Osservazioni

Per salvare il documento senza crittografia, questa proprietà dovrebbe essere`nullo` o stringa vuota.

### Esempi

Mostra come crittografare un documento ODT/OTT salvato con una password e quindi caricarlo utilizzando Aspose.Words.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un nuovo OdtSaveOptions e passa "SaveFormat.Odt",
 // o "SaveFormat.Ott" come formato in cui salvare il documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Se apriamo questo documento con un editor appropriato,
// ci chiederà la password che abbiamo specificato nell'oggetto SaveOptions.
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
* spazio dei nomi [Aspose.Words.Saving](../../odtsaveoptions/)
* assemblea [Aspose.Words](../../../)


