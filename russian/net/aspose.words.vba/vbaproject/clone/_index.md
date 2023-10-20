---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: VbaProject Clone метод. Выполняет копиюVbaProject  на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Выполняет копию[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Возвращаемое значение

Клонированный[`VbaProject`](../).

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

* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
