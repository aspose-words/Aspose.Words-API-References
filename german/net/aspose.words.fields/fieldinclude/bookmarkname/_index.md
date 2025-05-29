---
title: FieldInclude.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „FieldInclude BookmarkName“ Lesezeichen in Ihren Dokumenten einfach verwalten und so für mehr Organisation und Effizienz sorgen.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldinclude/bookmarkname/
---
## FieldInclude.BookmarkName property

Ruft den Namen des einzuschließenden Lesezeichens im Dokument ab oder legt ihn fest.

```csharp
public string BookmarkName { get; set; }
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
