---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Vba.VbaModuleType, die Modelltypen in VBA-Projekten für eine verbesserte Automatisierung und optimierte Dokumentenverwaltung definiert.
type: docs
weight: 7420
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
| DocumentModule | `0` | Ein Typ von VBA-Projektelement, das ein Modul für eingebettete Makros und programmgesteuerte Zugriffsvorgänge angibt, die einem Dokument zugeordnet sind. |
| ProceduralModule | `1` | Eine Sammlung von Unterprogrammen und Funktionen. |
| ClassModule | `2` | Ein Modul, das die Definition eines neuen Objekts enthält. Jede Instanz einer Klasse erzeugt ein neues Objekt. Die im Modul definierten Prozeduren werden zu Eigenschaften und Methoden des Objekts. |
| DesignerModule | `3` | Ein VBA-Modul, das die Methoden und Eigenschaften eines ActiveX-Steuerelements erweitert, das beim Projekt registriert wurde. |

## Beispiele

Zeigt, wie man mit Makros ein VBA-Projekt erstellt.

```csharp
Document doc = new Document();

// Erstellen Sie ein neues VBA-Projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Erstellen Sie ein neues Modul und geben Sie einen Makro-Quellcode an.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Fügen Sie das Modul zum VBA-Projekt hinzu.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Siehe auch

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)
