---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos durch Ihre Dokumente mit der MoveToField-Methode von DocumentBuilder. Sie ermöglicht eine schnelle Cursorbewegung zu jedem beliebigen Feld und verbessert so die Bearbeitungseffizienz.
type: docs
weight: 570
url: /de/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Bewegt den Cursor zu einem Feld im Dokument.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| field | Field | Das Feld, zu dem der Cursor bewegt werden soll. |
| isAfter | Boolean | Wann`WAHR` , verschiebt den Cursor hinter das Feldende. Wenn`FALSCH`, verschiebt den Cursor vor den Feldanfang. |

## Beispiele

Zeigt, wie der Cursor der Knoteneinfügemarke eines Dokumentgenerators in ein bestimmtes Feld verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie mit dem DocumentBuilder ein Feld ein und fügen Sie dahinter einen Textlauf hinzu.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Der Cursor des Builders befindet sich derzeit am Ende des Dokuments.
Assert.Null(builder.CurrentNode);

// Bewegen Sie den Cursor zum Feld und geben Sie dabei an, ob der Cursor vor oder nach dem Feld platziert werden soll.
builder.MoveToField(field, moveCursorToAfterTheField);

// Beachten Sie, dass sich der Cursor in beiden Fällen außerhalb des Feldes befindet.
// Das bedeutet, dass wir das Feld mit dem Builder auf diese Weise nicht bearbeiten können.
// Um ein Feld zu bearbeiten, können wir die MoveTo-Methode des Builders auf dem FieldStart eines Felds verwenden
// oder FieldSeparator-Knoten, um den Cursor darin zu platzieren.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Siehe auch

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
