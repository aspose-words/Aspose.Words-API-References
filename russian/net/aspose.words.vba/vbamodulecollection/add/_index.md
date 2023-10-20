---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words для .NET
description: VbaModuleCollection Add метод. Добавляет модуль в коллекцию на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Добавляет модуль в коллекцию.

```csharp
public void Add(VbaModule vbaModule)
```

## Примеры

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
