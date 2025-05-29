---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words para .NET
description: Descubra la propiedad UseLegacyOrder en FindReplaceOptions. Habilite las búsquedas de texto secuenciales para mayor precisión. El valor predeterminado es falso. ¡Optimice su procesamiento de texto!
type: docs
weight: 180
url: /es/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

True indica que se realiza una búsqueda de texto secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es`FALSO` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## Ejemplos

Muestra cómo cambiar el orden de búsqueda de los nodos al realizar una operación de búsqueda y reemplazo de texto.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte tres ejecuciones que podamos buscar usando un patrón de expresiones regulares.
    //Coloca una de esas carreras dentro de un cuadro de texto.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();

    // Asigna una devolución de llamada personalizada a la propiedad "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // Si establecemos la propiedad "UseLegacyOrder" en "verdadero",
    // La operación de búsqueda y reemplazo recorrerá todas las ejecuciones fuera de un cuadro de texto
    //antes de pasar por los que están dentro de un cuadro de texto.
    // Si establecemos la propiedad "UseLegacyOrder" en "falso",
    // La operación de búsqueda y reemplazo recorrerá todas las ejecuciones en un rango en orden secuencial.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// Registra el orden de todas las coincidencias que ocurren durante una operación de búsqueda y reemplazo.
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
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
