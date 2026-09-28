---
title: "Метод Aspose::Words::Document::RemoveCustomizations"
linktitle: "RemoveCustomizations"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::RemoveCustomizations. Удаляет настройки панели инструментов и клавиатурных команд из документа в C++."
type: docs
weight: 67750
url: /ru/cpp/aspose.words/document/removecustomizations/
---
## Document::RemoveCustomizations method


Удаляет настройки панелей инструментов и клавиатурных команд из документа.

```cpp
void Aspose::Words::Document::RemoveCustomizations()
```


## Примеры



Показывает, как удалить настройки панели инструментов и клавиатурных команд из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Customized menu.docx");

// Удалить все пользовательские настройки UI документа, включая пользовательские пункты контекстного меню.
doc->RemoveCustomizations();

doc->Save(get_ArtifactsDir() + u"Document.RemoveCustomizations.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
