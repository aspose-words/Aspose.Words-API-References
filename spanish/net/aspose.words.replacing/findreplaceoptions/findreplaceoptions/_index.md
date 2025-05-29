---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor FindReplaceOptions para inicializar fácilmente una nueva instancia con configuraciones predeterminadas, mejorando su funcionalidad de búsqueda y reemplazo.
type: docs
weight: 10
url: /es/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

Inicializa una nueva instancia de la clase FindReplaceOptions con la configuración predeterminada.

```csharp
public FindReplaceOptions()
```

## Ejemplos

Muestra cómo reconocer y utilizar sustituciones dentro de patrones de reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// El uso del modo heredado no admite muchas funciones avanzadas, por lo que debemos configurarlo como 'falso'.
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

Inicializa una nueva instancia de la clase FindReplaceOptions con la dirección especificada.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| direction | FindReplaceDirection | La dirección de la operación de buscar y reemplazar. |

### Ver también

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

Inicializa una nueva instancia de la clase FindReplaceOptions con la devolución de llamada de reemplazo especificada.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | La devolución de llamada que se utilizará para reemplazar el texto encontrado. |

## Ejemplos

Muestra cómo rastrear el orden en que una operación de reemplazo de texto recorre los nodos.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // El uso de un encabezado/pie de página diferente para la primera página afectará el orden de búsqueda.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Durante una operación de búsqueda y reemplazo, registra el contenido de cada nodo que tenga texto que la operación "encuentra".
/// en el estado en que se encontraba antes de que se realizara el reemplazo.
/// Esto mostrará el orden en que la operación de reemplazo de texto recorre los nodos.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Ver también

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

Inicializa una nueva instancia de la clase FindReplaceOptions con la dirección especificada y la devolución de llamada de reemplazo.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| direction | FindReplaceDirection | La dirección de la operación de buscar y reemplazar. |
| replacingCallback | IReplacingCallback | La devolución de llamada que se utilizará para reemplazar el texto encontrado. |

### Ver también

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
