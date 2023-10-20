---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words para .NET
description: Document CompatibilityOptions propiedad. Proporciona acceso a las opciones de compatibilidad de documentos es decir las preferencias de usuario ingresadas en elCompatibilidad pestaña delOpciones cuadro de diálogo en Word en C#.
type: docs
weight: 50
url: /es/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Proporciona acceso a las opciones de compatibilidad de documentos (es decir, las preferencias de usuario ingresadas en el**Compatibilidad** pestaña del**Opciones** cuadro de diálogo en Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

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

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
