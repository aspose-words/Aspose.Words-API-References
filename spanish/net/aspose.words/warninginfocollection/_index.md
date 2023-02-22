---
title: Class WarningInfoCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WarningInfoCollection clase. Representa una colección tipada deWarningInfo objetos.
type: docs
weight: 6330
url: /es/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Representa una colección tipada de[`WarningInfo`](../warninginfo/) objetos.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Obtiene el número de elementos que contiene la colección. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Obtiene un elemento en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Elimina todos los elementos de la colección. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todos los elementos de la colección. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(WarningInfo) | Implementa el[`IWarningCallback`](../iwarningcallback/) interfaz. Agrega una advertencia a esta colección. |

### Observaciones

Puede usar este objeto de colección como la forma más simple de[`IWarningCallback`](../iwarningcallback/)implementación para recopilar todas las advertencias que genera Aspose.Words durante una operación de carga o guardado. Cree una instancia de esta clase y asígnela al[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) o[`WarningCallback`](../documentbase/warningcallback/) propiedad.

### Ejemplos

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana para una fuente faltante de las fuentes de fuentes disponibles.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Abra un documento que contenga texto formateado con una fuente que no existe en ninguna de nuestras fuentes de fuentes.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Asigne una devolución de llamada para manejar las advertencias de sustitución de fuentes.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Establecer un nombre de fuente predeterminado y habilitar la sustitución de fuentes.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Obtendremos una advertencia de sustitución de fuente si guardamos un documento al que le falta una fuente.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // También podemos verificar las advertencias en la colección y borrarlas.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Llamado cada vez que ocurre una advertencia durante la carga/guardado.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Ver también

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


