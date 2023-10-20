---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words para .NET
description: Field Unlink método. Realiza la desvinculación del campo en C#.
type: docs
weight: 130
url: /es/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Realiza la desvinculación del campo.

```csharp
public bool Unlink()
```

### Valor_devuelto

`verdadero` si el campo ha sido desvinculado, en caso contrario`FALSO` .

## Observaciones

Reemplaza el campo con su resultado más reciente.

Algunos campos, como los campos XE (entrada de índice) y los campos SEQ (secuencia), no se pueden desvincular.

## Ejemplos

Muestra cómo desvincular un campo.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Ver también

* class [Field](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
