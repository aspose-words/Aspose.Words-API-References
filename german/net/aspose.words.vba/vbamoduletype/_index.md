---
title: Enum VbaModuleType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaModuleType opsomming. Gibt den Typ eines Modells in einem VBAProjekt an.
type: docs
weight: 6570
url: /de/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Gibt den Typ eines Modells in einem VBA-Projekt an.

```csharp
public enum VbaModuleType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DocumentModule | `0` | Ein VBA-Projektelementtyp, der ein Modul für eingebettete Makros und programmgesteuerte Zugriffsvorgänge angibt, die einem Dokument zugeordnet sind. |
| ProceduralModule | `1` | Eine Sammlung von Unterprogrammen und Funktionen. |
| ClassModule | `2` | Ein Modul, das die Definition für ein neues Objekt enthält. Jede Instanz einer Klasse erstellt ein neues Objekt, und Prozeduren, die im Modul definiert sind, werden zu Eigenschaften und Methoden des Objekts. |
| DesignerModule | `3` | Ein VBA-Modul, das die Methoden und Eigenschaften eines ActiveX-Steuerelements erweitert, das beim Projekt registriert wurde. |

### Beispiele

Zeigt, wie man ein VBA-Projekt mithilfe von Makros erstellt.

```csharp
Document doc = new Document();

// Ein neues VBA-Projekt erstellen.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Ein neues Modul erstellen und einen Makroquellcode angeben.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modul zum VBA-Projekt hinzufügen.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Siehe auch

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


