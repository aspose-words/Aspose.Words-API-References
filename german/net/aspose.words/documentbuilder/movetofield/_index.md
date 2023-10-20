---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words für .NET
description: DocumentBuilder MoveToField methode. Bewegt den Cursor auf ein Feld im Dokument in C#.
type: docs
weight: 530
url: /de/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Bewegt den Cursor auf ein Feld im Dokument.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| field | Field | Das Feld, zu dem der Cursor bewegt werden soll. |
| isAfter | Boolean | Wann`WAHR` , bewegt den Cursor hinter das Feldende. Wann`FALSCH`, bewegt den Cursor vor den Feldanfang. |

## Beispiele

Zeigt, wie der Knoteneinfügepunkt-Cursor eines Document Builders in ein bestimmtes Feld verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Mit dem DocumentBuilder ein Feld einfügen und danach eine Textzeile hinzufügen.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Der Cursor des Builders befindet sich derzeit am Ende des Dokuments.
Assert.Null(builder.CurrentNode);

// Bewegen Sie den Cursor auf das Feld und geben Sie dabei an, ob dieser Cursor vor oder nach dem Feld platziert werden soll.
builder.MoveToField(field, moveCursorToAfterTheField);

// Beachten Sie, dass sich der Cursor in beiden Fällen außerhalb des Feldes befindet.
// Das bedeutet, dass wir das Feld nicht auf diese Weise mit dem Builder bearbeiten können.
// Um ein Feld zu bearbeiten, können wir die MoveTo-Methode des Builders für den FieldStart eines Felds verwenden
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
