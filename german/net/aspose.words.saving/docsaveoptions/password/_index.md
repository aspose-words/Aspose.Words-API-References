---
title: DocSaveOptions.Password
second_title: Aspose.Words für .NET-API-Referenz
description: DocSaveOptions eigendom. Ruft ein Passwort ab/legt es fest um das Dokument mit der RC4Verschlüsselungsmethode zu verschlüsseln.
type: docs
weight: 30
url: /de/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Ruft ein Passwort ab/legt es fest, um das Dokument mit der RC4-Verschlüsselungsmethode zu verschlüsseln.

```csharp
public string Password { get; set; }
```

### Bemerkungen

Um das Dokument ohne Verschlüsselung zu speichern, sollte diese Eigenschaft null oder eine leere Zeichenfolge sein.

### Beispiele

Zeigt, wie Speicheroptionen für ältere Microsoft Word-Formate festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Legen Sie ein Passwort fest, das das Laden des Dokuments durch Microsoft Word oder Aspose.Words schützt.
// Beachten Sie, dass dadurch der Inhalt des Dokuments in keiner Weise verschlüsselt wird.
options.Password = "MyPassword";

// Wenn das Dokument einen Verteiler enthält, können wir ihn beim Speichern beibehalten, indem wir dieses Flag auf true setzen.
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
* namensraum [Aspose.Words.Saving](../../docsaveoptions/)
* Montage [Aspose.Words](../../../)


