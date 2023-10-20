---
title: MsWordVersion Enum
linktitle: MsWordVersion
articleTitle: MsWordVersion
second_title: Aspose.Words para .NET
description: Aspose.Words.Settings.MsWordVersion enumeración. Permite que Aspose.Wods imite el comportamiento de la aplicación específica de la versión de MS Word en C#.
type: docs
weight: 5860
url: /es/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Permite que Aspose.Wods imite el comportamiento de la aplicación específica de la versión de MS Word.

```csharp
public enum MsWordVersion
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Word2000 | `0` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2000. |
| Word2002 | `1` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2002. |
| Word2003 | `2` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2003. |
| Word2007 | `3` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2007. |
| Word2010 | `4` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2010. |
| Word2013 | `5` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2013. |
| Word2016 | `6` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2016. |
| Word2019 | `7` | Optimice el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2019. |

## Ejemplos

Muestra cómo optimizar el documento para diferentes versiones de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Este objeto contiene una lista extensa de indicadores únicos para cada documento
    // que nos permiten facilitar la compatibilidad con versiones anteriores de Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Imprime la configuración predeterminada para un documento en blanco.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Podemos acceder a estas configuraciones en Microsoft Word a través de "Archivo" -> "Opciones" -> "Avanzado" -> "Opciones de compatibilidad para...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Podemos utilizar el método OptimizeFor para garantizar una compatibilidad óptima con una versión específica de Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Agrupa todas las banderas en el objeto de opciones de compatibilidad de un documento por estado, luego imprime cada grupo.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings/)
* asamblea [Aspose.Words](../../)
