---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: VbaModule Clone метод. Выполняет копиюVbaModule  на С#.
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

## Примеры

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
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
