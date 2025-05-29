---
title: BuiltInDocumentProperties.RevisionNumber
linktitle: RevisionNumber
articleTitle: RevisionNumber
second_title: Aspose.Words für .NET
description: Verwalten Sie die Revisionsnummer Ihres Dokuments mit BuiltInDocumentProperties. Verfolgen Sie Änderungen ganz einfach und verbessern Sie die Versionskontrolle für eine bessere Zusammenarbeit.
type: docs
weight: 250
url: /de/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Ruft die Revisionsnummer des Dokuments ab oder legt sie fest.

```csharp
public int RevisionNumber { get; set; }
```

## Bemerkungen

Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele

Zeigt, wie mit REVNUM-Feldern gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Fügen Sie ein REVNUM-Feld ein, das die aktuelle Revisionsnummerneigenschaft des Dokuments anzeigt.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Diese Eigenschaft zählt, wie oft ein Dokument in Microsoft Word gespeichert wurde,
// und hat nichts mit verfolgten Revisionen zu tun. Wir finden es, indem wir im Windows Explorer mit der rechten Maustaste auf das Dokument klicken.
// über Eigenschaften -> Details. Wir können diese Eigenschaft manuell aktualisieren.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

Zeigt, wie mit Dokumenteigenschaften in der Kategorie „Ursprung“ gearbeitet wird.

```csharp
// Öffnen Sie ein Dokument, das wir mit Microsoft Word erstellt und bearbeitet haben.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Die folgenden integrierten Eigenschaften enthalten Informationen zur Erstellung und Bearbeitung dieses Dokuments.
// Wir können im Windows Explorer mit der rechten Maustaste auf dieses Dokument klicken und finden
// diese Eigenschaften über die Kategorie „Eigenschaften“ -> „Details“ -> „Herkunft“.
// Felder wie PRINTDATE und EDITTIME können diese Werte im Dokumenttext anzeigen.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Wir können auch die Werte integrierter Eigenschaften ändern.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word aktualisiert die folgenden Eigenschaften automatisch, wenn wir das Dokument speichern.
// Um diese Eigenschaften mit Aspose.Words zu verwenden, müssen wir die Werte manuell festlegen.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Wir können im Windows Explorer mit der rechten Maustaste auf dieses Dokument klicken und diese Eigenschaften unter „Eigenschaften“ -> „Details“ -> „Ursprung“ finden.
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
