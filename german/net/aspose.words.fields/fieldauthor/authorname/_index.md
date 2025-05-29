---
title: FieldAuthor.AuthorName
linktitle: AuthorName
articleTitle: AuthorName
second_title: Aspose.Words für .NET
description: Verwalten Sie Dokumentautoren mühelos mit FieldAuthor AuthorName. Rufen Sie Autorennamen einfach ab oder legen Sie sie fest, um die Glaubwürdigkeit und Organisation Ihrer Inhalte zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldauthor/authorname/
---
## FieldAuthor.AuthorName property

Ruft den Namen des Dokumentautors ab oder legt ihn fest.

```csharp
public string AuthorName { get; set; }
```

## Beispiele

Zeigt, wie ein AUTOR-Feld verwendet wird, um den Namen des Dokumenterstellers anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//AUTHOR-Felder beziehen ihre Ergebnisse aus der integrierten Dokumenteigenschaft „Author“.
// Wenn wir ein Dokument in Microsoft Word erstellen und speichern,
// In dieser Eigenschaft wird unser Benutzername stehen.
// Wenn wir jedoch ein Dokument programmgesteuert mit Aspose.Words erstellen,
// Die Eigenschaft „Autor“ ist standardmäßig eine leere Zeichenfolge.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Legen Sie einen Backup-Autorennamen für die zu verwendenden AUTHOR-Felder fest
// wenn die Eigenschaft „Autor“ eine leere Zeichenfolge enthält.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aktualisieren eines AUTHOR-Feldes, das einen Wert enthält
// wendet diesen Wert auf die integrierte Eigenschaft „Autor“ an.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Wenn Sie diese Eigenschaft ändern und dann das Feld AUTHOR aktualisieren, wird dieser Wert auf das Feld angewendet.
doc.BuiltInDocumentProperties.Author = "John Doe";
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Wenn wir ein AUTHOR-Feld aktualisieren, nachdem wir seine Eigenschaft "Name" geändert haben,
// dann zeigt das Feld den neuen Namen an und wendet den neuen Namen auf die integrierte Eigenschaft an.
field.AuthorName = "Jane Doe";
field.Update();

Assert.AreEqual(" AUTHOR  \"Jane Doe\"", field.GetFieldCode());
Assert.AreEqual("Jane Doe", field.Result);

// AUTHOR-Felder haben keinen Einfluss auf die DefaultDocumentAuthor-Eigenschaft.
Assert.AreEqual("Jane Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Joe Bloggs", doc.FieldOptions.DefaultDocumentAuthor);

doc.Save(ArtifactsDir + "Field.AUTHOR.docx");
```

### Siehe auch

* class [FieldAuthor](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
