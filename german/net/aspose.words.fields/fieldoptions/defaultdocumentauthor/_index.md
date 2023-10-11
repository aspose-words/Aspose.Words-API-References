---
title: FieldOptions.DefaultDocumentAuthor
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Standardnamen des Dokumentautors ab oder legt diesen fest. Wenn der Name des Autors bereits in den integrierten Dokumenteigenschaften angegeben ist wird diese Option nicht berücksichtigt.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldoptions/defaultdocumentauthor/
---
## FieldOptions.DefaultDocumentAuthor property

Ruft den Standardnamen des Dokumentautors ab oder legt diesen fest. Wenn der Name des Autors bereits in den integrierten Dokumenteigenschaften angegeben ist, wird diese Option nicht berücksichtigt.

```csharp
public string DefaultDocumentAuthor { get; set; }
```

### Beispiele

Zeigt, wie ein AUTHOR-Feld verwendet wird, um den Namen eines Dokumenterstellers anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// AUTHOR-Felder beziehen ihre Ergebnisse aus der integrierten Dokumenteigenschaft namens „Author“.
// Wenn wir ein Dokument in Microsoft Word erstellen und speichern,
// es wird unseren Benutzernamen in dieser Eigenschaft haben.
// Wenn wir jedoch ein Dokument programmgesteuert mit Aspose.Words erstellen,
// Die Eigenschaft „Autor“ ist standardmäßig eine leere Zeichenfolge.
Assert.AreEqual(string.Empty, doc.BuiltInDocumentProperties.Author);

// Legen Sie einen Backup-Autornamen für die zu verwendenden AUTHOR-Felder fest
// wenn die Eigenschaft „Autor“ einen leeren String enthält.
doc.FieldOptions.DefaultDocumentAuthor = "Joe Bloggs";

builder.Write("This document was created by ");
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("Joe Bloggs", field.Result);

// Aktualisieren eines AUTHOR-Feldes, das einen Wert enthält
// wendet diesen Wert auf die integrierte Eigenschaft „Author“ an.
Assert.AreEqual("Joe Bloggs", doc.BuiltInDocumentProperties.Author);

// Wenn Sie diese Eigenschaft ändern und dann das Feld AUTHOR aktualisieren, wird dieser Wert auf das Feld angewendet.
doc.BuiltInDocumentProperties.Author = "John Doe";      
field.Update();

Assert.AreEqual(" AUTHOR ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

// Wenn wir ein AUTHOR-Feld aktualisieren, nachdem wir seine Eigenschaft „Name“ geändert haben,
// Dann zeigt das Feld den neuen Namen an und wendet den neuen Namen auf die integrierte Eigenschaft an.
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

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


