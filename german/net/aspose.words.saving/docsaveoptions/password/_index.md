---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words für .NET
description: Sichern Sie Ihre Dokumente mit DocSaveOptions! Legen Sie einfach ein Passwort für die RC4-Verschlüsselung fest oder rufen Sie es ab, um Ihre vertraulichen Informationen zu schützen.
type: docs
weight: 40
url: /de/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Ruft ein Kennwort ab bzw. legt es fest, um das Dokument mit der RC4-Verschlüsselungsmethode zu verschlüsseln.

```csharp
public string Password { get; set; }
```

## Bemerkungen

Um das Dokument unverschlüsselt zu speichern, sollte diese Eigenschaft`null` oder eine leere Zeichenfolge.

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
