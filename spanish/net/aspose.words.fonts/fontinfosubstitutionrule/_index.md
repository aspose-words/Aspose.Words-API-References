---
title: Class FontInfoSubstitutionRule
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.FontInfoSubstitutionRule clase. Regla de sustitución de información de fuente.
type: docs
weight: 2760
url: /es/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Regla de sustitución de información de fuente.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Especifica si la regla está habilitada o no. |

### Observaciones

De acuerdo con esta regla, Aspose.Words evalúa todos los campos relacionados en[`FontInfo`](../fontinfo/) (Panose, Sig, etc.) para la fuente que falta y encuentra la coincidencia más cercana entre las fuentes de fuentes disponibles. Si[`FontInfo`](../fontinfo/) no está disponible para la fuente que falta, entonces no se hará nada.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


