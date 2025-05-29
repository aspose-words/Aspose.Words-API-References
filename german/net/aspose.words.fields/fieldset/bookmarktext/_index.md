---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „FieldSet BookmarkText“ einfach verwalten können, um Ihre Lesezeichen anzupassen und zu verbessern und so eine bessere Organisation und Zugänglichkeit zu erreichen.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Ruft den neuen Text des Lesezeichens ab oder legt ihn fest.

```csharp
public string BookmarkText { get; set; }
```

## Beispiele

Zeigt, wie Sie mit einem SET-Feld mit Lesezeichen versehenen Text erstellen und ihn dann mithilfe eines REF-Felds im Dokument anzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

    // Benennen Sie mit einem SET-Feld markierten Text.
// Dieses Feld bezieht sich auf das „Lesezeichen“, nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Verweisen Sie in einem REF-Feld per Namen auf das Lesezeichen und zeigen Sie seinen Inhalt an.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Siehe auch

* class [FieldSet](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
