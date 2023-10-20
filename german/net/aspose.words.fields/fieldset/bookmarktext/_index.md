---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words für .NET
description: FieldSet BookmarkText eigendom. Ruft den neuen Text des Lesezeichens ab oder legt ihn fest in C#.
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

Zeigt, wie Sie mit einem SET-Feld markierten Text erstellen und ihn dann mithilfe eines REF-Felds im Dokument anzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Mit einem Lesezeichen versehenen Text mit einem SET-Feld benennen.
// Dieses Feld bezieht sich auf das „Lesezeichen“, nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// In einem REF-Feld namentlich auf das Lesezeichen verweisen und seinen Inhalt anzeigen.
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
