---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words für .NET
description: Steuern Sie die Anzeige der Dateigröße mit der IsInMegabytes-Eigenschaft von FieldFileSize. Wechseln Sie einfach zwischen Bytes und Megabytes für mehr Übersichtlichkeit und Benutzerfreundlichkeit.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Ruft ab oder legt fest, ob die Dateigröße in Megabyte angezeigt werden soll.

```csharp
public bool IsInMegabytes { get; set; }
```

## Beispiele

Zeigt, wie die Dateigröße eines Dokuments mit einem FILESIZE-Feld angezeigt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Unten sind drei verschiedene Maßeinheiten
// mit denen FILESIZE-Felder die Dateigröße des Dokuments anzeigen können.
// 1 - Bytes:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Um die Werte dieser Felder während der Bearbeitung in Microsoft Word zu aktualisieren,
// Wir müssen zuerst die Änderungen speichern und diese Felder dann manuell aktualisieren.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Siehe auch

* class [FieldFileSize](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
