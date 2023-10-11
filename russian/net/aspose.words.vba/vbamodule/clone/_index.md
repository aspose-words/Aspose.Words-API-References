---
title: VbaModule.Clone
second_title: Справочник по API Aspose.Words для .NET
description: VbaModule метод. Выполняет копиюVbaModule .
type: docs
weight: 50
url: /ru/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Выполняет копию[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Возвращаемое значение

Клонированный[`VbaModule`](../).

### Примеры

Показывает, как выполнить глубокое клонирование проекта и модуля VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// В целевом документе у нас уже есть модуль с именем «Module1»
// потому что мы клонировали его вместе с проектом. Нам нужно будет удалить модуль.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Смотрите также

* class [VbaModule](../)
* пространство имен [Aspose.Words.Vba](../../vbamodule/)
* сборка [Aspose.Words](../../../)


