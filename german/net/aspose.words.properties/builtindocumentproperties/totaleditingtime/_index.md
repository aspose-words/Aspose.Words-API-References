---
title: BuiltInDocumentProperties.TotalEditingTime
linktitle: TotalEditingTime
articleTitle: TotalEditingTime
second_title: Aspose.Words für .NET
description: Entdecken Sie die TotalEditingTime-Eigenschaft von BuiltInDocumentProperties, um Dokumentbearbeitungen effizient zu verfolgen. Optimieren Sie Ihren Workflow mit präzisem Bearbeitungszeitmanagement.
type: docs
weight: 340
url: /de/net/aspose.words.properties/builtindocumentproperties/totaleditingtime/
---
## BuiltInDocumentProperties.TotalEditingTime property

Ruft die Gesamtbearbeitungszeit in Minuten ab oder legt sie fest.

```csharp
public int TotalEditingTime { get; set; }
```

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
