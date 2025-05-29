---
title: BuiltInDocumentProperties.CreatedTime
linktitle: CreatedTime
articleTitle: CreatedTime
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „CreatedTime“ von BuiltInDocumentProperties, um für eine bessere Organisation einfach auf das Erstellungsdatum Ihres Dokuments in UTC zuzugreifen und es zu verwalten.
type: docs
weight: 100
url: /de/net/aspose.words.properties/builtindocumentproperties/createdtime/
---
## BuiltInDocumentProperties.CreatedTime property

Ruft das Datum der Dokumenterstellung in UTC ab oder legt es fest.

```csharp
public DateTime CreatedTime { get; set; }
```

## Bemerkungen

Bei Dokumenten im RTF-Format gibt diese Eigenschaft die Ortszeit des Computers des Autors zum Zeitpunkt der Dokumenterstellung zurück.

Aspose.Words aktualisiert diese Eigenschaft nicht.

## Beispiele

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
