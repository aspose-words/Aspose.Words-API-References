---
title: OptimizeFor
second_title: Referencia de API de Aspose.Words para .NET
description: Permite optimizar el contenido del documento así como el comportamiento predeterminado de Aspose.Words para una versión particular de MS Word.
type: docs
weight: 720
url: /es/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Permite optimizar el contenido del documento, así como el comportamiento predeterminado de Aspose.Words para una versión particular de MS Word.

Utilice este método para evitar que MS Word muestre la cinta "Modo de compatibilidad" al cargar el documento. (Tenga en cuenta que es posible que también deba configurar el[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) propiedad a Iso29500_2008_Transitional o superior.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Ejemplos

Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Top" para
// alinear el texto en este cuadro de texto con el lado superior de la forma.
// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Middle" para
// alinear el texto en este cuadro de texto al centro de la forma.
// Establecer la propiedad "VerticalAnchor" en "TextBoxAnchor.Bottom" para
// alinea el texto de este cuadro de texto con la parte inferior de la forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible desde Microsoft Word 2007 en adelante.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Muestra cómo establecer una especificación de cumplimiento de OOXML para que se adhiera a un documento guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si configuramos opciones de compatibilidad para cumplir con Microsoft Word 2003,
// insertar una imagen definirá su forma usando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// El estándar OOXML "ISO/IEC 29500:2008" no admite formas VML.
// Si establecemos la propiedad "Compliance" del objeto SaveOptions en "OoxmlCompliance.Iso29500_2008_Strict",
  // cualquier documento que guardemos al pasar este objeto tendrá que seguir ese estándar.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Nuestro documento guardado define la forma usando DML para cumplir con el estándar OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Muestra cómo optimizar el documento para diferentes versiones de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Este objeto contiene una extensa lista de banderas únicas para cada documento
    // que nos permiten facilitar la retrocompatibilidad con versiones anteriores de Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Imprime la configuración predeterminada para un documento en blanco.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Podemos acceder a esta configuración en Microsoft Word a través de "Archivo" -> "Opciones" -> "Avanzado" -> "Opciones de compatibilidad para...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Podemos usar el método OptimizeFor para garantizar una compatibilidad óptima con una versión específica de Microsoft Word.
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

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* espacio de nombres [Aspose.Words.Settings](../../compatibilityoptions/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
