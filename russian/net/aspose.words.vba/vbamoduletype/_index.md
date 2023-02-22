---
title: Enum VbaModuleType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Vba.VbaModuleType перечисление. Указывает тип модели в проекте VBA.
type: docs
weight: 6260
url: /ru/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Указывает тип модели в проекте VBA.

```csharp
public enum VbaModuleType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| DocumentModule | `0` | Тип элемента проекта VBA, указывающий модуль для встроенных макросов и программных операций доступа , связанных с документом. |
| ProceduralModule | `1` | Набор подпрограмм и функций. |
| ClassModule | `2` | Модуль, содержащий определение нового объекта. Каждый экземпляр класса создает новый объект, и процедуры, определенные в модуле, становятся свойствами и методами объекта. |
| DesignerModule | `3` | Модуль VBA, который расширяет методы и свойства элемента управления ActiveX, зарегистрированного в проекте. |

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

* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)


