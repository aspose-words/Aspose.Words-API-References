---
title: OfficeMath.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words para .NET
description: Descubra el método de aceptación de OfficeMath para una gestión fluida de visitantes. Optimice su flujo de trabajo con una integración sencilla y una mayor eficiencia.
type: docs
weight: 60
url: /es/net/aspose.words.math/officemath/accept/
---
## OfficeMath.Accept method

Acepta un visitante.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| visitor | DocumentVisitor | El visitante que visitará los nodos. |

### Valor_devuelto

Verdadero si se visitaron todos los nodos; falso si[`DocumentVisitor`](../../../aspose.words/documentvisitor/) detuvo la operación antes de visitar todos los nodos.

## Observaciones

Enumera este nodo y todos sus hijos. Cada nodo llama a un método correspondiente en[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Para obtener más información, consulte el patrón de diseño Visitor.

Llamadas[`VisitOfficeMathStart`](../../../aspose.words/documentvisitor/visitofficemathstart/) , luego llama[`Accept`](../../../aspose.words/node/accept/) para todos los nodos secundarios de Office Math y las llamadas[`VisitOfficeMathEnd`](../../../aspose.words/documentvisitor/visitofficemathend/) al final.

## Ejemplos

Muestra cómo imprimir la estructura de nodos de cada nodo de matemáticas de oficina en un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante de documento, el visitante visita el nodo que lo acepta,
    // y luego recorre todos los nodos secundarios en profundidad.
    //El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Recorre el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos OfficeMath encontrados y sus hijos.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Obtiene el texto simple del documento que fue acumulado por el visitante.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo Ejecutar en el documento.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando se encuentra un nodo OfficeMath en el documento.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangrala dependiendo de qué tan profundo se encuentre el visitante en el árbol del documento.
    /// </summary>
    /// <param name="texto"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
