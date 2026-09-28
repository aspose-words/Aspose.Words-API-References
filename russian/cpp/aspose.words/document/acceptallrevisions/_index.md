---
title: "Aspose::Words::Document::AcceptAllRevisions метод"
linktitle: "AcceptAllRevisions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::AcceptAllRevisions метод. Принимает все отслеживаемые изменения в документе в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


Принимает все отслеживаемые изменения в документе.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## Примеры



Показывает, как принять все отслеживаемые изменения в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Отредактируйте документ с включённым отслеживанием изменений, чтобы создать несколько ревизий.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// Мы можем пройтись по каждой ревизии и принять/отклонить её как часть нашего документа.
// Если мы знаем, что хотим принять каждую ревизию, мы можем сделать это проще, вызвав этот метод.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
