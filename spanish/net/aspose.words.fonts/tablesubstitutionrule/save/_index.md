---
title: TableSubstitutionRule.Save
second_title: Referencia de API de Aspose.Words para .NET
description: TableSubstitutionRule método. Guarda la configuración actual de sustitución de tablas en el archivo.
type: docs
weight: 70
url: /es/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(string) {#save_1}

Guarda la configuración actual de sustitución de tablas en el archivo.

```csharp
public void Save(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo de salida. |

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

* class [TableSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* asamblea [Aspose.Words](../../../)

---

## Save(Stream) {#save}

Guarda la configuración actual de sustitución de tablas en stream.

```csharp
public void Save(Stream outputStream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputStream | Stream | Salida de corriente. |

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

* class [TableSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* asamblea [Aspose.Words](../../../)


