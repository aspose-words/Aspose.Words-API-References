---
title: DocumentBuilder.MoveToField
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Sposta il cursore su un campo nel documento.
type: docs
weight: 540
url: /it/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Sposta il cursore su un campo nel documento.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| field | Field | Il campo su cui spostare il cursore. |
| isAfter | Boolean | Quando`VERO` , sposta il cursore dopo la fine del campo. Quando`falso`, sposta il cursore prima dell'inizio del campo. |

### Esempi

Mostra come spostare il cursore del punto di inserimento del nodo di un generatore di documenti su un campo specifico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un campo utilizzando DocumentBuilder e aggiungi una sequenza di testo dopo di esso.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Il cursore del builder è attualmente alla fine del documento.
Assert.Null(builder.CurrentNode);

// Sposta il cursore sul campo specificando se posizionare il cursore prima o dopo il campo.
builder.MoveToField(field, moveCursorToAfterTheField);

// Nota che il cursore è fuori dal campo in entrambi i casi.
// Ciò significa che non possiamo modificare il campo utilizzando il builder in questo modo.
// Per modificare un campo, possiamo utilizzare il metodo MoveTo del builder sul FieldStart di un campo
// o il nodo FieldSeparator per posizionare il cursore all'interno.
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

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


