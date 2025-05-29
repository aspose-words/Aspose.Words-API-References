---
title: DocSaveOptions.SaveRoutingSlip
linktitle: SaveRoutingSlip
articleTitle: SaveRoutingSlip
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveRoutingSlip-Eigenschaft von DocSaveOptions. Steuern Sie die RoutingSlip-Datenspeicherung für Ihre Dokumente. Verbessern Sie die Ausgabeanpassung ganz einfach!
type: docs
weight: 70
url: /de/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

Wann`FALSCH` , Laufzetteldaten werden nicht im Ausgabedokument gespeichert. Der Standardwert ist`WAHR` .

```csharp
public bool SaveRoutingSlip { get; set; }
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

* class [DocSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
