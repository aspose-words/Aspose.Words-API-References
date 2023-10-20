---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words für .NET
description: OdtSaveOptions constructeur. Initialisiert eine neue Instanz dieser Klasse die zum Speichern eines Dokuments im verwendet werden kannOdt format in C#.
type: docs
weight: 10
url: /de/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt format.

```csharp
public OdtSaveOptions()
```

## Beispiele

Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Siehe auch

* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt format verschlüsselt mit einem Passwort.

```csharp
public OdtSaveOptions(string password)
```

### Siehe auch

* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kannOdt or Ott format.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | SaveFormat | Kann seinOdt oderOtt. |

## Beispiele

Zeigt, wie man ein gespeichertes ODT/OTT-Dokument mit einem Passwort verschlüsselt und es dann mit Aspose.Words lädt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie eine neue OdtSaveOptions und übergeben Sie entweder „SaveFormat.Odt“,
 // oder „SaveFormat.Ott“ als Format zum Speichern des Dokuments.
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Wenn wir dieses Dokument mit einem geeigneten Editor öffnen,
// Es wird uns zur Eingabe des Passworts auffordern, das wir im SaveOptions-Objekt angegeben haben.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Wenn wir dieses Dokument erneut mit Aspose.Words öffnen oder bearbeiten möchten,
// Wir müssen dem Ladekonstruktor ein LoadOptions-Objekt mit dem richtigen Passwort bereitstellen.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
