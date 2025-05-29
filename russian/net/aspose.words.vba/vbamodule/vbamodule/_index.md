---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words для .NET
description: Создавайте пустые модули VBA без усилий с помощью нашего конструктора VbaModule. Оптимизируйте процесс кодирования и улучшите рабочий процесс разработки уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Создает пустой модуль.

```csharp
public VbaModule()
```

## Примеры

Показывает, как создать проект VBA с использованием макросов.

```csharp
Document doc = new Document();

// Создать новый проект VBA.
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

* class [VbaModule](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
