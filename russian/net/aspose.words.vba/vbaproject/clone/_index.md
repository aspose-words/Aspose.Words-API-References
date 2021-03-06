---
title: Clone
second_title: Справочник по API Aspose.Words для .NET
description: Выполняет копированиеVbaProjectaspose.words.vba/vbaproject .
type: docs
weight: 70
url: /ru/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Выполняет копирование[`VbaProject`](../../vbaproject) .

```csharp
public VbaProject Clone()
```

### Возвращаемое значение

Клонированный VbaProject.

### Примеры

Показывает, как выполнить глубокое клонирование проекта и модуля VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// В целевом документе у нас уже есть модуль с именем "Module1"
// потому что мы его клонировали вместе с проектом. Нам нужно будет удалить модуль.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Смотрите также

* class [VbaProject](../../vbaproject)
* пространство имен [Aspose.Words.Vba](../../vbaproject)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
