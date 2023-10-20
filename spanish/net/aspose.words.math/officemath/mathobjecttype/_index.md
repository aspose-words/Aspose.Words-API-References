---
title: OfficeMath.MathObjectType
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words para .NET
description: OfficeMath MathObjectType propiedad. Obtiene el tipoMathObjectType de este objeto de Office Math en C#.
type: docs
weight: 30
url: /es/net/aspose.words.math/officemath/mathobjecttype/
---
## OfficeMath.MathObjectType property

Obtiene el tipo`MathObjectType` de este objeto de Office Math.

```csharp
public MathObjectType MathObjectType { get; }
```

## Ejemplos

Muestra cómo imprimir la estructura de nodos de cada nodo matemático de Office en un documento.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Cuando conseguimos que un nodo compuesto acepte un visitante del documento, el visitante visita el nodo receptor,
    // y luego atraviesa todos los hijos del nodo en profundidad.
    // El visitante puede leer y modificar cada nodo visitado.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Atraviesa el árbol no binario de nodos secundarios de un nodo.
/// Crea un mapa en forma de cadena de todos los nodos de OfficeMath encontrados y sus hijos.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Obtiene el texto sin formato del documento acumulado por el visitante.
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
    /// Se llama después de que se hayan visitado todos los nodos secundarios de un nodo de OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Agrega una línea al StringBuilder y sangra dependiendo de qué tan profundo esté el visitante en el árbol del documento.
    /// </summary>
    /// <param nombre="texto"></param>
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

* enum [MathObjectType](../../mathobjecttype/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
