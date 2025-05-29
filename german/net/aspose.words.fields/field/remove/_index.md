---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos Felder aus Dokumenten mit der Methode „Field Remove“. Erhalten Sie präzise Knotenrückgaben und verarbeiten Sie leere Felder nahtlos. Optimieren Sie Ihren Workflow!
type: docs
weight: 120
url: /de/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` .

```csharp
public Node Remove()
```

## Beispiele

Zeigt, wie Felder aus einer Feldsammlung entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Unten sind vier Möglichkeiten zum Entfernen von Feldern aus einer Feldsammlung aufgeführt.
// 1 - Ein Feld dazu bringen, sich selbst zu entfernen:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 – Lassen Sie die Sammlung ein Feld entfernen, das wir an ihre Entfernungsmethode übergeben:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 – Entfernen Sie ein Feld aus einer Sammlung an einem Index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 – Entfernen Sie alle Felder auf einmal aus der Sammlung:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Zeigt, wie PRIVATE-Felder verarbeitet werden.

```csharp
public void FieldPrivate()
{
    // Öffnen Sie ein Corel WordPerfect-Dokument, das wir in das DOCX-Format konvertiert haben.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x-Dokumente wie das von uns geladene können PRIVATE-Felder enthalten.
    // Microsoft Word behält PRIVATE-Felder während Lade-/Speichervorgängen bei,
    // bietet aber keine Funktionalität für sie.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Wir können auch PRIVATE-Felder mithilfe eines Dokumentgenerators einfügen.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Diese Felder sind keine praktikable Möglichkeit, vertrauliche Informationen zu schützen.
    // Sofern keine Abwärtskompatibilität mit älteren Versionen von WordPerfect erforderlich ist,
    // Wir können diese Felder sicher entfernen. Dies können wir mithilfe einer DocumentVisiitor-Implementierung tun.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Entfernt alle gefundenen PRIVATE-Felder.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein FieldEnd-Knoten gefunden wird.
    /// Wenn der Knoten zu einem PRIVATE-Feld gehört, wird das gesamte Feld entfernt.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Siehe auch

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
