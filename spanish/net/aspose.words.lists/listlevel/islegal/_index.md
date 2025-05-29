---
title: ListLevel.IsLegal
linktitle: IsLegal
articleTitle: IsLegal
second_title: Aspose.Words para .NET
description: Descubra ListLevel IsLegal. Controle fácilmente los estilos de números heredados. Elija el árabe para una apariencia moderna o conserve los estilos originales para un toque clásico.
type: docs
weight: 50
url: /es/net/aspose.words.lists/listlevel/islegal/
---
## ListLevel.IsLegal property

Verdadero si el nivel convierte todos los números heredados a árabes, falso si conserva su estilo numérico.

```csharp
public bool IsLegal { get; set; }
```

## Ejemplos

Muestra formas avanzadas de personalizar las etiquetas de listas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Las etiquetas de nivel 1 se formatearán de acuerdo con el estilo de párrafo "Título 1" y tendrán un prefijo.
// Estos se verán como "Apéndice A", "Apéndice B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Las etiquetas de nivel 2 mostrarán los números actuales del primer y segundo nivel de lista y tendrán ceros a la izquierda.
// Si el primer nivel de lista está en 1, entonces las etiquetas de lista de estos se verán así: "Sección (1.01)", "Sección (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Tenga en cuenta que el nivel superior utiliza numeración en mayúsculas.
//Podemos configurar la propiedad "IsLegal" para utilizar números arábigos para los niveles de lista superiores.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Las etiquetas de nivel 3 serán números romanos en mayúsculas con un prefijo y un sufijo y se reiniciarán en cada elemento de nivel 1 de lista.
// Estas etiquetas de lista se verán así: "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Poner en negrita las etiquetas de todos los niveles de lista.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Aplicar formato de lista al párrafo actual.
builder.ListFormat.List = list;

// Cree elementos de lista que mostrarán los tres niveles de nuestra lista.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Ver también

* class [ListLevel](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
