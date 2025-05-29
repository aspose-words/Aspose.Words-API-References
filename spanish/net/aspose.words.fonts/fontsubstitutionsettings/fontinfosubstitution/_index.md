---
title: FontSubstitutionSettings.FontInfoSubstitution
linktitle: FontInfoSubstitution
articleTitle: FontInfoSubstitution
second_title: Aspose.Words para .NET
description: Descubra cómo FontSubstitutionSettings mejora su tipografía con reglas de información de fuente personalizables para un mejor diseño y legibilidad.
type: docs
weight: 30
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/
---
## FontSubstitutionSettings.FontInfoSubstitution property

Configuraciones relacionadas con la regla de sustitución de información de fuente.

```csharp
public FontInfoSubstitutionRule FontInfoSubstitution { get; }
```

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

* class [FontInfoSubstitutionRule](../../fontinfosubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
