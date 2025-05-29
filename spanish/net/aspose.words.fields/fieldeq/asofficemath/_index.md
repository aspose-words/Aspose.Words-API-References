---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words para .NET
description: Transforme los campos EQ con el método AsOfficeMath de FieldEQ, convirtiéndolos sin esfuerzo en objetos de Office Math para una integración perfecta de documentos.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Devuelve el objeto Office Math correspondiente al campo EQ.

```csharp
public OfficeMath AsOfficeMath()
```

### Valor_devuelto

Devuelve`nulo` Si el código de campo está vacío o no es válido, de lo contrario[`OfficeMath`](../../../aspose.words.math/officemath/) instancia.

## Ejemplos

Muestra cómo reemplazar el campo EQ con Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Ver también

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
