---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words per .NET
description: OdtSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt formato in C#.
type: docs
weight: 10
url: /it/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt formato.

```csharp
public OdtSaveOptions()
```

## Esempi

Mostra come rendere un documento salvato conforme a uno schema ODT precedente.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt format crittografato con una password.

```csharp
public OdtSaveOptions(string password)
```

### Guarda anche

* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileOdt oppure Ott formato.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | SaveFormat | Può essereOdt OOtt. |

## Esempi

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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
