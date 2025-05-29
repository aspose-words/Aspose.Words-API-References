---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words per .NET
description: Esplora senza sforzo i tuoi documenti con il metodo MoveToField di DocumentBuilder, che consente di spostare rapidamente il cursore su qualsiasi campo per una maggiore efficienza di modifica.
type: docs
weight: 570
url: /it/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Sposta il cursore su un campo nel documento.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| field | Field | Campo su cui spostare il cursore. |
| isAfter | Boolean | Quando`VERO` , sposta il cursore dopo la fine del campo. Quando`falso`, sposta il cursore prima dell'inizio del campo. |

## Esempi

Mostra come spostare il cursore del punto di inserimento del nodo di un generatore di documenti su un campo specifico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un campo utilizzando DocumentBuilder e aggiungere una sequenza di testo dopo di esso.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Il cursore del builder si trova attualmente alla fine del documento.
Assert.Null(builder.CurrentNode);

// Sposta il cursore sul campo specificando se posizionarlo prima o dopo il campo.
builder.MoveToField(field, moveCursorToAfterTheField);

// Nota che in entrambi i casi il cursore si trova all'esterno del campo.
// Ciò significa che non possiamo modificare il campo utilizzando il builder in questo modo.
// Per modificare un campo, possiamo usare il metodo MoveTo del builder sul FieldStart di un campo
// o nodo FieldSeparator in cui posizionare il cursore.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
