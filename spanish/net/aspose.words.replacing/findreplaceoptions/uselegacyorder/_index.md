---
title: FindReplaceOptions.UseLegacyOrder
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Verdadero indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado esFALSO .
type: docs
weight: 170
url: /es/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

Verdadero indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es`FALSO` .

```csharp
public bool UseLegacyOrder { get; set; }
```

### Ejemplos

Muestra cómo cambiar el orden de búsqueda de los nodos al realizar una operación de buscar y reemplazar texto.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserta tres ejecuciones que podamos buscar usando un patrón de expresiones regulares.
    // Coloca una de esas ejecuciones dentro de un cuadro de texto.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
    FindReplaceOptions options = new FindReplaceOptions();

    // Asigne una devolución de llamada personalizada a la propiedad "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Si configuramos la propiedad "UseLegacyOrder" en "true", el
    // la operación de buscar y reemplazar recorrerá todas las ejecuciones fuera de un cuadro de texto
    // antes de revisar los que están dentro de un cuadro de texto.
    // Si configuramos la propiedad "UseLegacyOrder" en "false", el
    // la operación de buscar y reemplazar recorrerá todas las ejecuciones en un rango en orden secuencial.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Registra el orden de todas las coincidencias que ocurren durante una operación de buscar y reemplazar.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


