---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words para .NET
description: Descubra el método Field Unlink para desvincular campos sin esfuerzo, mejorando su gestión de datos y agilizando su flujo de trabajo para obtener resultados óptimos.
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

`verdadero` si el campo ha sido desvinculado, de lo contrario`FALSO` .

## Observaciones

Reemplaza el campo con su resultado más reciente.

Algunos campos, como los campos XE (Entrada de índice) y los campos SEQ (Secuencia), no se pueden desvincular.

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
