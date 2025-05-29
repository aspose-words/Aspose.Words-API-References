---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words para .NET
description: Mejore sus documentos sin esfuerzo con el método Range UpdateFields, actualizando los valores de campo de manera rápida y eficiente para una mayor precisión.
type: docs
weight: 130
url: /es/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Actualiza los valores de los campos del documento en este rango.

```csharp
public void UpdateFields()
```

## Observaciones

Cuando abre, modifica y luego guarda un documento, Aspose.Words no actualiza los campos automáticamente, sino que los mantiene intactos. Por lo tanto, generalmente querrá llamar a este método antes de guardar si ha modificado el documento programáticamente y desea asegurarse de que los valores de campo (calculados) adecuados aparezcan en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es un tipo de actualización de campo y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campo. Para obtener una lista detallada de los tipos de campo admitidos, consulte la Guía del programador.

Este método no actualiza los campos relacionados con los algoritmos de diseño de página (por ejemplo, PAGE, PAGES, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando se representa un documento o se llama a un método.[`UpdatePageLayout`](../../document/updatepagelayout/).

Para actualizar campos en todo el documento utilice[`UpdateFields`](../../document/updatefields/).

## Ejemplos

Muestra cómo actualizar todos los campos de un rango.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Los campos DOCPROPERTY anteriores mostrarán el valor de esta propiedad de documento incorporada.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Si actualizamos el valor de una propiedad de un documento, necesitaremos actualizar todos los campos DOCPROPERTY para mostrarlo.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

//Actualiza todos los campos que están en el rango de la primera sección.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Ver también

* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
