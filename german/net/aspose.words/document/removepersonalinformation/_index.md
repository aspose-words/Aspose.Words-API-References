---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words für .NET
description: Sorgen Sie mit der Funktion „Dokument-RemovePersonalInformation“ in Word für Datenschutz. Benutzerdaten aus Kommentaren und Eigenschaften werden beim Speichern automatisch gelöscht.
type: docs
weight: 360
url: /de/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Ruft ein Flag ab oder legt es fest, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Revisionen und Dokumenteigenschaften entfernt.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Beispiele

Zeigt, wie das Entfernen persönlicher Informationen während einer manuellen Speicherung aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie Inhalte mit persönlichen Informationen ein.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Dieses Flag entspricht Datei -> Optionen -> Trust Center -> Trust Center-Einstellungen... ->
// Datenschutzoptionen -> „Persönliche Informationen beim Speichern aus den Dateieigenschaften entfernen“ in Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Diese Option wird während eines Speichervorgangs mit Aspose.Words nicht wirksam.
// Personenbezogene Daten werden aus unserem Dokument mit gesetztem Flag entfernt, wenn wir es manuell mit Microsoft Word speichern.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
