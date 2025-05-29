---
title: TableSubstitutionRule.LoadLinuxSettings
linktitle: LoadLinuxSettings
articleTitle: LoadLinuxSettings
second_title: Aspose.Words para .NET
description: Cargue fácilmente configuraciones de sustitución de tablas predefinidas para Linux con el método LoadLinuxSettings. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule.LoadLinuxSettings method

Carga configuraciones de sustitución de tablas predefinidas para la plataforma Linux.

```csharp
public void LoadLinuxSettings()
```

## Ejemplos

Muestra cómo acceder a las tablas de sustitución de fuentes para Windows y Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Cree una nueva regla de sustitución de tabla y cargue la tabla de sustitución de fuentes predeterminada de Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// En Windows, el sustituto predeterminado para la fuente "Times New Roman CE" es "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

//Podemos guardar la tabla en forma de documento XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux tiene su propia tabla de sustitución.
//Existen múltiples fuentes sustitutas para "Times New Roman CE".
// Si el primer sustituto, "FreeSerif", tampoco está disponible,
// esta regla recorrerá las demás en la matriz hasta encontrar una disponible.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Guarde la tabla de sustitución de Linux en forma de un documento XML mediante una secuencia.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Ver también

* class [TableSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
