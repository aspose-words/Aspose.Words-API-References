---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von DocSaveOptions, um einfach zwischen den Formaten Doc und Dot für nahtloses Speichern von Dokumenten zu wählen. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinDoc oderDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie Speicheroptionen für ältere Microsoft Word-Formate festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Legen Sie ein Kennwort fest, das das Laden des Dokuments durch Microsoft Word oder Aspose.Words schützt.
// Beachten Sie, dass der Inhalt des Dokuments dadurch in keiner Weise verschlüsselt wird.
options.Password = "MyPassword";

// Wenn das Dokument einen Laufzettel enthält, können wir ihn beim Speichern beibehalten, indem wir dieses Flag auf „true“ setzen.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Um das Dokument laden zu können,
// Wir müssen das Passwort, das wir im DocSaveOptions-Objekt angegeben haben, in einem LoadOptions-Objekt anwenden.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
