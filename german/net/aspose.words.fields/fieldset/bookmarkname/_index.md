---
title: FieldSet.BookmarkName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldSet eigendom. Ruft den Namen des Lesezeichens ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Ruft den Namen des Lesezeichens ab oder legt ihn fest.

```csharp
public string BookmarkName { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words.Fields](../../fieldset/)
* Montage [Aspose.Words](../../../)


