---
title: BuiltInDocumentProperties.Category
linktitle: Category
articleTitle: Category
second_title: Aspose.Words für .NET
description: Verwalten Sie die Kategorie Ihres Dokuments mühelos mit BuiltInDocumentProperties. Passen Sie die Dokumentorganisation einfach an und verbessern Sie sie für einen besseren Workflow.
type: docs
weight: 30
url: /de/net/aspose.words.properties/builtindocumentproperties/category/
---
## BuiltInDocumentProperties.Category property

Ruft die Kategorie des Dokuments ab oder legt sie fest.

```csharp
public string Category { get; set; }
```

## Beispiele

Zeigt, wie mit integrierten Dokumenteigenschaften in der Kategorie „Beschreibung“ gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Unten sind vier integrierte Dokumenteigenschaften aufgeführt, die über Felder verfügen, deren Werte im Dokumenttext angezeigt werden können.
// 1 - Eigenschaft „Autor“, die wir mithilfe eines AUTHOR-Felds anzeigen können:
properties.Author = "John Doe";
builder.Write("Author:\t");
builder.InsertField(FieldType.FieldAuthor, true);

// 2 - Eigenschaft „Titel“, die wir mithilfe eines TITLE-Felds anzeigen können:
properties.Title = "John's Document";
builder.Write("\nDoc title:\t");
builder.InsertField(FieldType.FieldTitle, true);

// 3 - Eigenschaft „Betreff“, die wir mithilfe eines SUBJECT-Felds anzeigen können:
properties.Subject = "My subject";
builder.Write("\nSubject:\t");
builder.InsertField(FieldType.FieldSubject, true);

// 4 - Eigenschaft „Kommentare“, die wir mithilfe eines KOMMENTAR-Felds anzeigen können:
properties.Comments = $"This is {properties.Author}'s document about {properties.Subject}";
builder.Write("\nComments:\t\"");
builder.InsertField(FieldType.FieldComments, true);
builder.Write("\"");

// Die integrierte Eigenschaft „Kategorie“ verfügt nicht über ein Feld, das ihren Wert anzeigen kann.
properties.Category = "My category";

// Wir können mehrere Schlüsselwörter für ein Dokument festlegen, indem wir den Zeichenfolgenwert der Eigenschaft „Schlüsselwörter“ durch Semikolons trennen.
properties.Keywords = "Tag 1; Tag 2; Tag 3";

// Wir können im Windows Explorer mit der rechten Maustaste auf dieses Dokument klicken und diese Eigenschaften unter „Eigenschaften“ -> „Details“ finden.
// Die integrierte Eigenschaft „Autor“ befindet sich in der Gruppe „Ursprung“ und die anderen in der Gruppe „Beschreibung“.
doc.Save(ArtifactsDir + "DocumentProperties.Description.docx");
```

### Siehe auch

* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
