---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words für .NET
description: Entdecken Sie die IncludeFullPath-Eigenschaft von FieldFileName und verwalten Sie Dateipfade ganz einfach mit anpassbaren Einstellungen für eine verbesserte Dateiverwaltung und -organisation.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Ruft ab oder legt fest, ob der vollständige Dateipfadname eingeschlossen werden soll.

```csharp
public bool IncludeFullPath { get; set; }
```

## Beispiele

Zeigt, wie Sie mit FieldOptions den Standardwert für das Feld FILENAME überschreiben.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Dieses Feld FILENAME zeigt den lokalen Systemdateinamen des von uns geladenen Dokuments an.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Standardmäßig zeigt das Feld FILENAME den Namen der Datei an, jedoch nicht den vollständigen lokalen Dateisystempfad.
// Wir können ein Flag setzen, damit der vollständige Dateipfad angezeigt wird.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Wir können für diese Eigenschaft auch einen Wert festlegen auf
// überschreibe den Wert, der im Feld FILENAME angezeigt wird.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Siehe auch

* class [FieldFileName](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
