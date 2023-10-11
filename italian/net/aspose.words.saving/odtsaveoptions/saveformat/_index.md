---
title: OdtSaveOptions.SaveFormat
second_title: Aspose.Words per .NET API Reference
description: OdtSaveOptions proprietà. Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto opzioni di salvataggio. Può essereOdt OOtt .
type: docs
weight: 50
url: /it/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto opzioni di salvataggio. Può essereOdt OOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../odtsaveoptions/)
* assemblea [Aspose.Words](../../../)


