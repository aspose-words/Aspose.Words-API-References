---
title: AbsolutePositionTab
second_title: Referencia de API de Aspose.Words para .NET
description: Una pestaña de posición absoluta es un carácter que se utiliza para avanzar la posición en la línea de texto actual cuando se muestra este contenido de WordprocessingML.
type: docs
weight: 10
url: /es/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Una pestaña de posición absoluta es un carácter que se utiliza para avanzar la posición en la línea de texto actual cuando se muestra este contenido de WordprocessingML.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [Font](../../aspose.words/inline/font/) { get; } | Proporciona acceso al formato de fuente de este objeto. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Devuelve verdadero si este nodo puede contener otros nodos. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Devuelve verdadero si este objeto se eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Devuelve verdadero si este objeto se insertó en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Devoluciones **verdadero** si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | Devoluciones **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Recupera el padre[`Paragraph`](../paragraph/) de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(DocumentVisitor) | Acepta un visitante. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Obtiene el carácter especial que representa este nodo. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Ejemplos

Muestra cómo procesar caracteres de tabulación de posición absoluta con un visitante del documento.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extraiga el contenido de texto de nuestro documento aceptando este visitante de documento personalizado.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // La tabulación de posición absoluta, que no tiene equivalente en forma de cadena, se ha convertido explícitamente en un carácter de tabulación.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Una AbsolutePositionTab también puede aceptar un DocumentVisitor por sí misma.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Recopila el contenido de texto de todas las ejecuciones en el documento visitado. Reemplaza todos los caracteres de tabulación absolutos con tabulaciones ordinarias.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando se encuentra un nodo AbsolutePositionTab en el documento.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega texto a la salida actual. Respeta el indicador de salida activado/desactivado.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Texto sin formato del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [SpecialChar](../specialchar/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
