---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство VbaModule Type, определите свои модули как процедурные, документные, классовые или конструкторские для расширенной функциональности и организации.
type: docs
weight: 40
url: /ru/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Указывает, является ли модуль процедурным модулем, модулем документа, модулем класса или модулем дизайнера.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
