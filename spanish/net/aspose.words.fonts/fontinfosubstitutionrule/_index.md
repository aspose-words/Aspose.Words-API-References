---
title: FontInfoSubstitutionRule Class
linktitle: FontInfoSubstitutionRule
articleTitle: FontInfoSubstitutionRule
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.FontInfoSubstitutionRule para optimizar la gestión de fuentes en sus documentos con capacidades de sustitución perfectas.
type: docs
weight: 3370
url: /es/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Regla de sustitución de información de fuente.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Especifica si la regla está habilitada o no. |

## Observaciones

Según esta regla, Aspose.Words evalúa todos los campos relacionados en[`FontInfo`](../fontinfo/) (Panose, Sig, etc.) busca la fuente faltante y encuentra la más cercana entre las fuentes disponibles. Si[`FontInfo`](../fontinfo/) no está disponible para la fuente faltante, entonces no se hará nada.

## Ejemplos

Muestra cómo configurar la propiedad para encontrar la coincidencia más cercana para una fuente faltante entre las fuentes de fuentes disponibles.

```csharp
public void EnableFontSubstitution()
{
    // Abra un documento que contenga texto formateado con una fuente que no existe en ninguna de nuestras fuentes de fuentes.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Asignar una devolución de llamada para manejar advertencias de sustitución de fuentes.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Establezca un nombre de fuente predeterminado y habilite la sustitución de fuente.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Las métricas de fuente originales deben utilizarse después de la sustitución de la fuente.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    //Recibiremos una advertencia de sustitución de fuente si guardamos un documento con una fuente faltante.
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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Se llama cada vez que ocurre una advertencia durante la carga/guardado.
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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
