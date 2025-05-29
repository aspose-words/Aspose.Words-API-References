---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words para .NET
description: Optimice su proceso de combinación de correspondencia con la propiedad TrimWhitespaces, garantizando datos limpios al eliminar espacios iniciales y finales para obtener resultados precisos.
type: docs
weight: 130
url: /es/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Obtiene o establece un valor que indica si los espacios iniciales y finales se eliminan de los valores de combinación de correspondencia.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Observaciones

El valor predeterminado es`verdadero` .

## Ejemplos

Muestra cómo recortar espacios en blanco de los valores de una fuente de datos mientras se ejecuta una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
