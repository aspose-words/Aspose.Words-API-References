---
title: "Aspose::Words::Style::get_Locked метод"
linktitle: "get_Locked"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_Locked метод. Указывает, заблокирован ли этот стиль в C++."
type: docs
weight: 13500
url: /ru/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Указывает, заблокирован ли этот стиль.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Примеры



Показывает, как заблокировать стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
