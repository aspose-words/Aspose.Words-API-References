---
title: FieldInclude.LockFields
second_title: Aspose.Words für .NET-API-Referenz
description: FieldInclude eigendom. Ruft ab oder legt fest ob verhindert werden soll dass Felder im eingeschlossenen Dokument aktualisiert werden.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Ruft ab oder legt fest, ob verhindert werden soll, dass Felder im eingeschlossenen Dokument aktualisiert werden.

```csharp
public bool LockFields { get; set; }
```

### Beispiele

Zeigt, wie ein INCLUDE-Feld erstellt und seine Eigenschaften festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können ein INCLUDE-Feld verwenden, um einen Teil eines anderen Dokuments in das lokale Dateisystem zu importieren.
// Das Lesezeichen aus dem anderen Dokument, auf das wir mit diesem Feld verweisen, enthält diesen importierten Teil.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Siehe auch

* class [FieldInclude](../)
* namensraum [Aspose.Words.Fields](../../fieldinclude/)
* Montage [Aspose.Words](../../../)


