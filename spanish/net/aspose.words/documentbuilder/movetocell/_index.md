---
title: DocumentBuilder.MoveToCell
linktitle: MoveToCell
articleTitle: MoveToCell
second_title: Aspose.Words para .NET
description: Navegue sin esfuerzo por su documento con el método MoveToCell de DocumentBuilder, posicionando rápidamente el cursor en cualquier celda de la tabla para una edición mejorada.
type: docs
weight: 540
url: /es/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Mueve el cursor a una celda de la tabla en la sección actual.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| tableIndex | Int32 | El índice de la tabla a la que moverse. |
| rowIndex | Int32 | El índice de la fila en la tabla. |
| columnIndex | Int32 | El índice de la columna en la tabla. |
| characterIndex | Int32 | Índice del carácter dentro de la celda. Un valor negativo permite especificar una posición desde el final de la celda. Use -1 para ir al final de la celda. |

## Observaciones

La navegación se realiza dentro de la historia actual de la sección actual.

Para los parámetros de índice, si el índice es mayor o igual a 0, se especifica un índice desde al inicio, siendo 0 el primer elemento. Si el índice es menor que 0, se especifica un índice desde al final, siendo -1 el último elemento.

## Ejemplos

Muestra cómo mover el cursor de un generador de documentos a una celda de una tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabla vacía de 2x2.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Debido a que hemos finalizado la tabla con el método EndTable,
//El cursor del generador de documentos está actualmente fuera de la tabla.
// Este cursor tiene la misma función que el cursor de texto parpadeante de Microsoft Word.
// También se puede mover a una ubicación diferente en el documento usando los métodos MoveTo del constructor.
//Podemos mover el cursor nuevamente dentro de la tabla a una celda específica.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
