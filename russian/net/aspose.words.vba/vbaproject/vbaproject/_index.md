---
title: VbaProject.VbaProject
second_title: Справочник по API Aspose.Words для .NET
description: VbaProject строитель. Создает пустой VbaProject.
type: docs
weight: 10
url: /ru/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Создает пустой VbaProject.

```csharp
public VbaProject()
```

### Примеры

Показывает, как создать проект VBA с помощью макросов.

```csharp
Document doc = new Document();

// Создаем новый проект VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Создаем новый модуль и указываем исходный код макроса.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Добавляем модуль в проект VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Смотрите также

* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../vbaproject/)
* сборка [Aspose.Words](../../../)


