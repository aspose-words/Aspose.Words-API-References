---
title: FieldOptions.FileName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Dateinamen des Dokuments ab oder setzt ihn.
type: docs
weight: 120
url: /de/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Ruft den Dateinamen des Dokuments ab oder setzt ihn.

```csharp
public string FileName { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird von der verwendet[`FieldFileName`](../../fieldfilename/) Feld mit höherer Priorität als das[`OriginalFileName`](../../../aspose.words/document/originalfilename/) Eigentum.

### Beispiele

Zeigt, wie FieldOptions verwendet wird, um den Standardwert für das Feld FILENAME zu überschreiben.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Dieses FILENAME-Feld zeigt den Dateinamen des lokalen Systems des geladenen Dokuments an.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Standardmäßig zeigt das Feld FILENAME den Namen der Datei, aber nicht ihren vollständigen lokalen Dateisystempfad.
// Wir können ein Flag setzen, damit es den vollständigen Dateipfad anzeigt.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Wir können auch einen Wert für diese Eigenschaft setzen auf
// Wert überschreiben, der im Feld FILENAME angezeigt wird.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


