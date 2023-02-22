---
title: Class TableSubstitutionRule
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.TableSubstitutionRule clase. Regla de sustitución de fuente de tabla.
type: docs
weight: 2880
url: /es/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Regla de sustitución de fuente de tabla.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Especifica si la regla está habilitada o no. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | Agrega nombres de fuente sustitutos para el nombre de fuente original dado. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | Devuelve una matriz que contiene nombres de fuente sustitutos para el nombre de fuente original especificado. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | Carga la configuración de sustitución de tablas desde el flujo XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | Carga la configuración de sustitución de tablas desde un archivo XML. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Carga la configuración de sustitución de tablas predefinida para la plataforma Linux. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Carga la configuración de sustitución de tablas predefinida para la plataforma Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Carga la configuración de sustitución de tablas predefinida para la plataforma Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | Guarda la configuración actual de sustitución de tablas en stream. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | Guarda la configuración actual de sustitución de tablas en el archivo. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | Anula los nombres de fuente sustitutos para el nombre de fuente original dado. |

### Observaciones

Esta regla define la lista de nombres de fuentes sustitutas que se utilizarán si la fuente original no está disponible. Se comprobarán las sustitutas para el nombre de la fuente y el[`AltName`](../fontinfo/altname/) (si lo hay).

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
// Si el primer sustituto, "FreeSerif" tampoco está disponible,
// esta regla recorrerá las demás en la matriz hasta que encuentre una disponible.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Guarde la tabla de sustitución de Linux en forma de documento XML mediante un flujo.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Ver también

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


