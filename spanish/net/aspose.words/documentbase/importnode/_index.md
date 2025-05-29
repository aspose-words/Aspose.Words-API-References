---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words para .NET
description: Importa nodos fácilmente desde otros documentos para optimizar tu flujo de trabajo con el método ImportNode de DocumentBase. ¡Optimiza tu gestión documental hoy mismo!
type: docs
weight: 110
url: /es/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Importa un nodo de otro documento al documento actual.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcNode | Node | El nodo que se está importando. |
| isImportChildren | Boolean | `verdadero` para importar todos los nodos secundarios de forma recursiva; de lo contrario,`FALSO`. |

### Valor_devuelto

El nodo clonado que pertenece al documento actual.

## Observaciones

Este método utiliza elUseDestinationStyles Opción para resolver el formato.

Al importar un nodo, se crea una copia del nodo de origen perteneciente al documento importador. El nodo devuelto no tiene padre. El nodo de origen no se modifica ni se elimina del documento original.

Antes de insertar un nodo de otro documento en este, debe importarse. Durante la importación, las propiedades específicas del documento, como las referencias a estilos y listas, se traducen del original al documento de importación. Una vez importado el nodo, se puede insertar en el lugar correspondiente del documento mediante[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Si el nodo de origen ya pertenece al documento de destino, entonces simplemente se crea un clone profundo del nodo de origen.

## Ejemplos

Muestra cómo importar un nodo de un documento a otro.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Cada nodo tiene un documento padre, que es el documento que contiene el nodo.
// Insertar un nodo en un documento al que el nodo no pertenece generará una excepción.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Utilice el método ImportNode para crear una copia de un nodo, que tendrá el documento
// que llamó al método ImportNode y lo estableció como su nuevo propietario del documento.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

//Ahora podemos insertar el nodo en el documento.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Ver también

* class [Node](../../node/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Importa un nodo de otro documento al documento actual con una opción para controlar el formato.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcNode | Node | El nodo a importar. |
| isImportChildren | Boolean | `verdadero` para importar todos los nodos secundarios de forma recursiva; de lo contrario,`FALSO`. |
| importFormatMode | ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |

### Valor_devuelto

El nodo clonado e importado. Pertenece al documento de destino, pero no tiene padre.

## Observaciones

Esta sobrecarga es útil para controlar cómo se importan los estilos y el formato de la lista.

Al importar un nodo, se crea una copia del nodo de origen perteneciente al documento importador. El nodo devuelto no tiene padre. El nodo de origen no se modifica ni se elimina del documento original.

Antes de insertar un nodo de otro documento en este, debe importarse. Durante la importación, las propiedades específicas del documento, como las referencias a estilos y listas, se traducen del original al documento de importación. Una vez importado el nodo, se puede insertar en el lugar correspondiente del documento mediante[`InsertBefore`](../../compositenode/insertbefore/) o [`InsertAfter`](../../compositenode/insertafter/).

Si el nodo de origen ya pertenece al documento de destino, entonces simplemente se crea un clone profundo del nodo de origen.

## Ejemplos

Muestra cómo importar un nodo del documento de origen al documento de destino con opciones específicas.

```csharp
// Cree dos documentos y agregue un estilo de carácter a cada documento.
// Configure los estilos para que tengan el mismo nombre, pero diferente formato de texto.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Importa la Sección del documento de destino al documento de origen, lo que provoca una colisión de nombres de estilo.
// Si usamos estilos de destino, entonces el texto fuente importado con el mismo nombre de estilo
// como texto de destino adoptará el estilo de destino.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Si usamos ImportFormatMode.KeepDifferentStyles, se conserva el estilo de origen,
// y el conflicto de nombres se resuelve agregando un sufijo.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Ver también

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
