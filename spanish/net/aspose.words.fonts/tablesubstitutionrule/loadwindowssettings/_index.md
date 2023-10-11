---
title: TableSubstitutionRule.LoadWindowsSettings
second_title: Referencia de API de Aspose.Words para .NET
description: TableSubstitutionRule método. Carga la configuración de sustitución de tablas predefinida para la plataforma Windows.
type: docs
weight: 60
url: /es/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

Carga la configuración de sustitución de tablas predefinida para la plataforma Windows.

```csharp
public void LoadWindowsSettings()
```

### Ejemplos

Muestra cómo acceder a las tablas de sustitución de fuentes para Windows y Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Cree una nueva regla de sustitución de tablas y cargue la tabla de sustitución de fuentes predeterminada de Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// En Windows, el sustituto predeterminado de la fuente "Times New Roman CE" es "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Podemos guardar la tabla en forma de documento XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux tiene su propia tabla de sustitución.
// Hay varias fuentes sustitutas para "Times New Roman CE".
// Si el primer sustituto, "FreeSerif", tampoco está disponible,
// esta regla recorrerá las demás en la matriz hasta encontrar una disponible.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Guarde la tabla de sustitución de Linux en forma de documento XML mediante una secuencia.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Ver también

* class [TableSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* asamblea [Aspose.Words](../../../)


