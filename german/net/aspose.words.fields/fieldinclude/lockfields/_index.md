---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words für .NET
description: Verwalten Sie Dokumentaktualisierungen mühelos mit der Eigenschaft FieldInclude LockFields. Steuern Sie die Feldbearbeitung und verbessern Sie die Dokumentintegrität mühelos.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Ruft ab oder legt fest, ob die Aktualisierung von Feldern im eingeschlossenen Dokument verhindert werden soll.

```csharp
public bool LockFields { get; set; }
```

## Beispiele

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
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
